# Claude API Basics -- Programmatic Access

> **What you will learn:** How to make your first API call to Claude, understand key parameters, and manage costs.
> **Prerequisites:** [Meet Claude](02-meet-claude.md), basic comfort with a terminal or Python
> **Time:** 15 minutes

## What Is the Claude API?

The **API** (Application Programming Interface) lets you use Claude programmatically -- from your own code, scripts, or applications. Instead of chatting through a web interface, you send requests and receive responses through code.

### When you need the API

| Use Case | Example |
|----------|---------|
| **Automation** | Process 500 customer emails automatically |
| **Building apps** | Add AI chat to your web or mobile app |
| **Batch processing** | Analyze a folder of documents overnight |
| **Custom workflows** | Connect Claude to your internal tools |
| **Prototyping** | Test prompt strategies programmatically |

## Getting Started

### Step 1: Create an Anthropic account

Go to [console.anthropic.com](https://console.anthropic.com) and create an account (separate from your claude.ai account).

### Step 2: Get an API key

1. Navigate to **API Keys** in the console
2. Click **Create Key**
3. Copy the key and store it securely (you will not see it again)
4. **Never put API keys in code that gets committed to git** -- use environment variables

```bash
# Set your API key as an environment variable
export ANTHROPIC_API_KEY="sk-ant-your-key-here"
```

### Step 3: Install the SDK

```bash
# Python
pip install anthropic

# Node.js / TypeScript
npm install @anthropic-ai/sdk
```

## Your First API Call

### Using Python

```python
import anthropic

client = anthropic.Anthropic()

message = client.messages.create(
    model="claude-sonnet-5",
    max_tokens=1024,
    messages=[
        {"role": "user", "content": "What is the capital of France?"}
    ]
)

print(message.content[0].text)
```

### Using curl

```bash
curl https://api.anthropic.com/v1/messages \
  -H "Content-Type: application/json" \
  -H "x-api-key: $ANTHROPIC_API_KEY" \
  -H "anthropic-version: 2023-06-01" \
  -d '{
    "model": "claude-sonnet-5",
    "max_tokens": 1024,
    "messages": [
      {"role": "user", "content": "What is the capital of France?"}
    ]
  }'
```

## Key Parameters

| Parameter | What It Controls | Example Values |
|-----------|-----------------|----------------|
| `model` | Which Claude model to use | `claude-sonnet-5`, `claude-opus-4-8`, `claude-haiku-4-5-20251001` |
| `max_tokens` | Maximum length of Claude's response | `256`, `1024`, `4096` |
| `temperature` | Randomness (0 = focused, 1 = creative) | `0` for factual, `0.7` for creative |
| `system` | System prompt (Claude's role/instructions) | `"You are a helpful assistant"` |
| `messages` | The conversation history | Array of user/assistant message pairs |

### Choosing a model

| Model | Best For | Speed | Cost |
|-------|----------|-------|------|
| **Haiku** | Simple tasks, classification, extraction | Fastest | Lowest |
| **Sonnet** | Most tasks -- good balance of quality and speed | Fast | Medium |
| **Opus** | Complex reasoning, nuanced analysis, difficult tasks | Slower | Highest |

Start with Sonnet for most use cases. Use Haiku when speed and cost matter more than depth. Use Opus when quality is paramount.

### Using a system prompt

```python
message = client.messages.create(
    model="claude-sonnet-5",
    max_tokens=1024,
    system="You are a concise technical writer. Always respond in "
           "3 sentences or fewer. Use precise language.",
    messages=[
        {"role": "user", "content": "Explain what an API is."}
    ]
)
```

### Multi-turn conversations

Send the full conversation history to maintain context:

```python
message = client.messages.create(
    model="claude-sonnet-5",
    max_tokens=1024,
    messages=[
        {"role": "user", "content": "My name is Alex."},
        {"role": "assistant", "content": "Hello Alex! How can I help you?"},
        {"role": "user", "content": "What is my name?"}
    ]
)
# Claude will respond: "Your name is Alex."
```

## Understanding Costs

API usage is billed per token (roughly 3/4 of a word).

| Cost Type | What It Measures |
|-----------|-----------------|
| **Input tokens** | Your messages + system prompt + conversation history |
| **Output tokens** | Claude's response (more expensive than input) |

**Cost control tips:**
- Use `max_tokens` to cap response length
- Choose the smallest model that meets your quality needs
- Use shorter system prompts when possible
- Start new conversations instead of sending very long histories

Check current pricing at [anthropic.com/pricing](https://www.anthropic.com/pricing).

## Rate Limits

The API has rate limits based on your usage tier:

- **Requests per minute** -- how many API calls you can make
- **Tokens per minute** -- total tokens processed per minute
- **Tokens per day** -- daily cap on total usage

If you hit a rate limit, the API returns a `429` error. Handle this in your code:

```python
import time
import anthropic

client = anthropic.Anthropic()

def call_claude(prompt, retries=3):
    for attempt in range(retries):
        try:
            return client.messages.create(
                model="claude-sonnet-5",
                max_tokens=1024,
                messages=[{"role": "user", "content": prompt}]
            )
        except anthropic.RateLimitError:
            if attempt < retries - 1:
                time.sleep(2 ** attempt)
            else:
                raise
```

### Try It Yourself

**Exercise 1: Make your first API call**

1. Create an account at console.anthropic.com
2. Generate an API key
3. Install the Python SDK (`pip install anthropic`)
4. Run the "Your First API Call" example above

**Exercise 2: Experiment with parameters**

Using the same setup, try:
1. Change `temperature` from `0` to `1` and ask the same question twice -- notice the variation
2. Change `max_tokens` to `50` and see how responses get cut short
3. Add a system prompt and observe how it changes behavior

**Exercise 3: Build a simple script**

Write a Python script that:
1. Reads a text file from your computer
2. Sends its content to Claude with the prompt "Summarize this in 3 bullet points"
3. Prints the summary

## Key Takeaways

- The API lets you use Claude from your own code, scripts, and applications
- Get an API key from console.anthropic.com (keep it secret, use environment variables)
- Start with Claude Sonnet for most tasks -- it balances quality, speed, and cost
- Key parameters: `model`, `max_tokens`, `temperature`, `system`, `messages`
- API usage is billed per token -- use `max_tokens` and model selection to control costs
- Send full conversation history in `messages` to maintain context across turns

## Next Steps

You have completed the tutorial series. For deeper reference material, check out:
- [Frameworks and Strategies](../docs/frameworks-and-strategies.md) -- strategic frameworks for getting the most out of Claude
- [Prompt Template Library](../docs/prompt-templates.md) -- ready-to-use prompt templates for common tasks
