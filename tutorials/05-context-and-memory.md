# Context and Memory -- How Claude Thinks

> **What you will learn:** How Claude processes your conversation, why it forgets between chats, and how to provide context effectively.
> **Prerequisites:** [Your First Conversation](04-your-first-conversation.md)
> **Time:** 10 minutes

## Claude Has No Long-Term Memory (By Default)

Each conversation with Claude starts from scratch. When you close a chat and open a new one, Claude has zero recollection of what you discussed before.

This is different from how you might expect a human assistant to work. There is no "memory" carrying over. Every new conversation is a blank slate.

**Why?** Privacy and predictability. Your conversations are not used to train Claude, and a fresh start means Claude's behavior is consistent and not influenced by unrelated past chats.

## What Is a Context Window?

The **context window** is the total amount of text Claude can "see" at once during a conversation. Think of it like a desk -- there is only so much paper you can spread out before things start falling off the edges.

Claude's context window is approximately **200,000 tokens** (roughly 150,000 words, or about 500 pages of text). This is one of the largest context windows available in any AI model.

### What counts toward context?

Everything in the current conversation:

| What Counts | Example |
|-------------|---------|
| Your messages | Every prompt you have typed |
| Claude's responses | Every reply Claude has generated |
| Uploaded files | PDFs, images, code files you have attached |
| System instructions | Project-level or custom instructions |

As the conversation grows, older parts may get less attention from Claude, even if they are technically still within the window.

## How to Provide Context Effectively

Claude works dramatically better when you give it relevant information up front, rather than expecting it to guess.

### Be specific, not vague

| Instead of... | Try... |
|--------------|--------|
| "Help me with my project" | "I'm building a Python Flask app that manages a to-do list. Here's my current code: [paste code]" |
| "Fix this" | "This function should return a sorted list, but it returns None. Here's the error message: [paste error]" |
| "Write something about marketing" | "Write a 200-word LinkedIn post announcing our new product launch. Target audience: small business owners. Tone: professional but approachable." |

### Paste relevant material directly

Claude can read and reason about text you paste into the conversation. When you need Claude to work with specific information:

- **Paste the actual text** rather than describing it vaguely
- **Include error messages** in full when debugging
- **Attach files** (PDFs, images, code) when available

### Set the scene early

The first message in a conversation sets the tone. A strong opener includes:

1. **Who you are** (your role or situation)
2. **What you need** (the specific task)
3. **What you are working with** (the relevant context)

Example:
```text
I'm a marketing manager writing our Q3 report for the leadership team.
I need to summarize these campaign results into 3 key takeaways.
Here are the results: [paste data]
```

## When Conversations Get Too Long

Signs that your conversation context is getting stretched:

- Claude starts repeating things it said earlier
- Claude "forgets" instructions you gave at the beginning
- Responses become less precise or more generic

**What to do:** Start a fresh conversation. Copy your most important context (key instructions, latest version of your work) into the first message of the new chat.

## Projects: Persistent Context Across Conversations

**Claude Projects** solve the memory problem for ongoing work. A project gives you:

- **Uploaded knowledge** -- PDFs, documents, code files that persist across conversations
- **Project instructions** -- custom behavior rules that apply to every conversation in that project
- **Conversation history** -- easy access to past chats within the project

You will learn how to set up Projects in the next tutorial.

### Try It Yourself

**Exercise 1: Observe the memory gap**
1. Start a conversation and tell Claude: "My name is Alex and I work at a company called Sunrise Tech."
2. Have a brief exchange (ask Claude anything)
3. Close the conversation and start a brand new one
4. Ask: "What is my name and where do I work?"
5. Notice that Claude has no idea

**Exercise 2: Compare with and without context**
1. Ask Claude: "Is this a good approach?" (with no other context)
2. Now ask: "I'm building a mobile app for tracking daily habits. I plan to use React Native for cross-platform support. Is this a good approach for a solo developer with JavaScript experience?"
3. Compare the quality and specificity of both responses

## Key Takeaways

- Claude starts every new conversation with zero memory of past chats
- The context window (~200K tokens) is the total text Claude can see at once in a conversation
- Providing specific, relevant context dramatically improves output quality
- When conversations get too long, start fresh and bring your key context forward
- Claude Projects provide persistent context across multiple conversations

## Next Steps

Learn how to set up Projects for persistent knowledge in [Projects and Knowledge](07-projects-and-knowledge.md), or jump to [Prompt Engineering Basics](06-prompt-engineering-basics.md) to learn how to write better prompts.
