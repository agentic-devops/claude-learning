# Meet Claude -- What Makes It Different

> **What you will learn:** What Claude is, who makes it, what it can do, and how it compares to other AI assistants.
> **Prerequisites:** [What Is AI and How Do Large Language Models Work?](01-what-is-ai.md)
> **Time:** 10 minutes

## Who Makes Claude?

Claude is made by **Anthropic**, a company founded in 2021 with a focus on AI safety. Anthropic's goal is to build AI systems that are reliable, interpretable, and steerable. This safety-first approach influences how Claude behaves -- it tends to be thoughtful, honest about uncertainty, and careful with sensitive topics rather than simply telling you what you want to hear.

## The Claude Model Family

As of 2025, Claude comes in three model sizes, each designed for different use cases:

| Model | Strengths | Best For |
|---|---|---|
| **Opus** | Most capable, deepest reasoning, best at complex analysis | Research, nuanced writing, multi-step problem solving |
| **Sonnet** | Balanced speed and capability, strong all-around | Most everyday tasks, coding, writing, analysis |
| **Haiku** | Fastest responses, lowest cost | Simple questions, quick lookups, high-volume tasks |

**Which should you use?** Start with **Sonnet**. It handles the vast majority of tasks well. Switch to Opus when you need deeper reasoning on a complex problem, or to Haiku when you need quick, simple answers.

## What Claude Can Do

### Strong Capabilities

- **Long document analysis**: Claude can read and work with up to 200,000 tokens at once -- roughly a 500-page book. You can upload entire reports, codebases, or manuscripts and ask questions about them.

- **Writing and editing**: From emails to essays to technical documentation, Claude produces clear, well-structured text. It is particularly good at matching a requested tone or style.

- **Code generation and debugging**: Claude can write code in dozens of programming languages, explain existing code, find bugs, and suggest improvements.

- **Reasoning and analysis**: Claude can break down complex problems, compare options, and walk through logic step by step.

- **Image understanding**: You can share images with Claude, and it will describe, analyze, or answer questions about what it sees.

- **Tool use**: Claude can use external tools and integrations (called **MCP**, or Model Context Protocol) to connect with other software and data sources.

### Honest Limitations

No AI is perfect. Here is what Claude cannot do or struggles with:

- **No persistent memory**: By default, each conversation starts fresh. Claude does not remember what you discussed yesterday unless you tell it again. (Projects and memory features can partially address this.)

- **Knowledge cutoff**: Claude's training data has a cutoff date. It may not know about very recent events.

- **No web browsing**: In its base mode, Claude cannot search the internet or visit websites. It works only with what you provide and what it learned during training.

- **Math and calculation errors**: While Claude can reason about math, it can make arithmetic mistakes. For critical calculations, ask it to show its work or double-check with a calculator.

- **Hallucination risk**: Like all LLMs, Claude can sometimes generate confident-sounding but incorrect information. Always verify important facts.

## Pricing Tiers

Claude is available at several pricing levels:

| Tier | Cost | What You Get |
|---|---|---|
| **Free** | $0 | Limited messages per day, access to Sonnet |
| **Pro** | $20/month | Higher message limits, access to Opus and Sonnet, priority access, early features |
| **Team** | $25/user/month | Everything in Pro plus team collaboration, admin controls, higher limits |
| **Enterprise** | Custom pricing | Advanced security, SSO, custom deployment, highest limits |

For most individuals just getting started, the **free tier** is a great way to explore. If you find yourself hitting message limits regularly, **Pro** is worth the upgrade.

## How Claude Compares to Other AI Assistants

You may have heard of other AI assistants like ChatGPT (by OpenAI) and Gemini (by Google). Here is an honest comparison:

| Feature | Claude | ChatGPT | Gemini |
|---|---|---|---|
| Long document handling | Excellent (200K tokens) | Good (128K tokens) | Good (up to 1M tokens) |
| Nuanced writing quality | Excellent | Very good | Good |
| Careful reasoning | Excellent | Very good | Good |
| Web browsing | Limited | Built-in | Built-in |
| Image generation | Not available | Built-in (DALL-E) | Built-in (Imagen) |
| Code generation | Excellent | Excellent | Very good |
| Safety and honesty | Strong focus | Good | Good |
| Ecosystem/plugins | Growing (MCP) | Large | Google integration |

**Where Claude excels**: If you value thoughtful writing, careful analysis of long documents, honest handling of uncertainty, and strong coding assistance, Claude is an excellent choice. It is particularly good at tasks where nuance and accuracy matter more than speed.

**Where others may be better**: If you need built-in web search or image generation as part of the same tool, ChatGPT or Gemini may be more convenient today.

The best approach is to try multiple tools and see which fits your workflow. There is no single "best" AI -- it depends on what you need.

## Claude's Personality

You will notice that Claude has a distinct communication style:

- It is direct and clear rather than verbose
- It admits when it is unsure rather than guessing
- It asks for clarification rather than making assumptions
- It can be warm and even witty, but stays focused on being helpful
- It will decline requests that are harmful or unethical, and explain why

This is by design. Anthropic has trained Claude to be a **helpful, harmless, and honest** assistant.

### Try It Yourself

Open a conversation with Claude and copy-paste this prompt:

```
What are your three biggest strengths and three biggest limitations? Be specific and honest -- I want to know where I can rely on you and where I should be careful.
```

Read the response carefully. Notice how Claude handles the question about its own limitations -- a good AI assistant should be transparent about what it cannot do.

Then try this follow-up:

```
If I could only use you for three types of tasks, which three would give me the most value? Why?
```

## Key Takeaways

- Claude is built by Anthropic with a focus on safety, honesty, and helpfulness
- Three model sizes exist: **Opus** (most capable), **Sonnet** (balanced), and **Haiku** (fastest) -- start with Sonnet
- Claude excels at long documents, nuanced writing, code, and careful reasoning
- Key limitations include no persistent memory, no web browsing, and the possibility of errors
- Claude is one of several excellent AI tools -- the best choice depends on your specific needs

## Next Steps

Ready to start using Claude? Continue to [Getting Started -- Accessing Claude](03-getting-started.md).
