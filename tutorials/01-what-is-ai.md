# What Is AI and How Do Large Language Models Work?

> **What you will learn:** What artificial intelligence actually means today and how large language models like Claude process and generate text.
> **Prerequisites:** None
> **Time:** 10 minutes

## What AI Actually Means

When most people hear "artificial intelligence," they picture robots from movies. The reality is far more practical and far less dramatic.

**Artificial intelligence (AI)** is software that can perform tasks that normally require human thinking -- recognizing patterns, understanding language, making decisions, and generating new content. The AI you will interact with today is not a sentient being. It is a sophisticated program that processes text and produces useful responses.

Modern AI is built around **machine learning**, a technique where software improves by learning from large amounts of data rather than being explicitly programmed with rules.

## What Is a Large Language Model?

A **Large Language Model (LLM)** is a specific type of AI that has been trained on enormous amounts of text -- books, articles, websites, code, and more. Through this training, the model learns patterns in language: grammar, facts, reasoning styles, and how ideas connect.

At its core, an LLM works by predicting the most likely next words in a sequence. When you ask it a question, it generates a response one piece at a time, choosing each piece based on everything that came before it.

Think of it this way: an LLM is like an extremely well-read research assistant who has read billions of pages. They can discuss nearly any topic fluently, but they might occasionally confuse details or fill gaps with plausible-sounding guesses -- because they are drawing on patterns, not looking things up in a database.

## Key Concepts Explained Simply

### Tokens

A **token** is the smallest unit of text that an LLM processes. Tokens are not exactly words -- they are chunks of text that the model breaks language into.

- A short common word like "the" is one token
- A longer word like "comfortable" might be split into two tokens
- As a rough rule: **one token is about 3/4 of a word**

**Example:** The phrase "Hello, world!" is about 4 tokens.

Why does this matter? Because models have limits on how many tokens they can handle, and pricing is based on token count.

### Context Window

The **context window** is the total amount of text the model can "see" at one time -- both what you send and what it responds with.

Think of it like a desk: you can only spread out so many papers before things start falling off the edge. Claude has a context window of **200,000 tokens**, which is roughly equivalent to a 500-page book. This is one of the largest context windows available, meaning Claude can work with very long documents in a single conversation.

### Temperature

**Temperature** is a setting that controls how random or creative the model's responses are.

| Temperature | Behavior | Best For |
|---|---|---|
| Low (0.0 - 0.3) | Predictable, focused, consistent | Factual questions, code, data analysis |
| Medium (0.5 - 0.7) | Balanced | General conversation, writing assistance |
| High (0.8 - 1.0) | Creative, varied, surprising | Brainstorming, creative writing, exploring ideas |

Most of the time, you do not need to worry about temperature -- the default settings work well for general use.

### Hallucination

**Hallucination** is when an AI generates information that sounds plausible and confident but is actually incorrect. This happens because the model is predicting likely text based on patterns, not looking up verified facts.

Examples of hallucinations:
- Citing a research paper that does not exist
- Giving a confident but wrong answer to a math problem
- Inventing historical events that never happened

This is the most important limitation to understand. **Always verify critical information**, especially facts, statistics, and citations.

## What LLMs Can and Cannot Do

| Can Do Well | Cannot Do |
|---|---|
| Explain concepts clearly | Access the internet in real time |
| Write and edit text | Remember previous conversations (by default) |
| Generate and debug code | Guarantee 100% factual accuracy |
| Analyze long documents | Perform actions in the real world |
| Translate languages | Have opinions or feelings |
| Brainstorm ideas | Know events after their training cutoff |

## How Is This Different from a Search Engine?

A search engine finds existing web pages that match your keywords. An LLM generates a new, original response tailored to your specific question. You can ask follow-up questions, request a different format, or have a back-and-forth dialogue -- things a search engine cannot do.

However, a search engine links to sources you can verify. An LLM typically does not, which is why critical thinking remains essential.

### Try It Yourself

Open Claude at [claude.ai](https://claude.ai) and try these prompts:

1. Copy and paste this prompt:
   ```
   Explain what you are in one paragraph, using simple language that a teenager could understand.
   ```

2. Then ask this follow-up:
   ```
   What happens when you don't know the answer to something? Be honest.
   ```

3. Notice how Claude responds -- it should be transparent about its limitations rather than making something up.

## Key Takeaways

- AI is practical software that processes language, not a science fiction robot
- Large Language Models work by predicting the most likely next words based on patterns learned from vast amounts of text
- Key terms to remember: **tokens** (text chunks), **context window** (how much text fits), **temperature** (creativity dial), and **hallucination** (plausible but wrong output)
- Always verify important facts from AI -- treat it as a helpful assistant, not an infallible authority

## Next Steps

Now that you understand how LLMs work, learn about the specific model you will be using: [Meet Claude -- What Makes It Different](02-meet-claude.md).
