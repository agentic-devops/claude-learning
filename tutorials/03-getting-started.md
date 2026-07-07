# Getting Started -- Accessing Claude

> **What you will learn:** The different ways to access Claude and how to set up your account and navigate the interface.
> **Prerequisites:** [Meet Claude -- What Makes It Different](02-meet-claude.md)
> **Time:** 10 minutes

## Five Ways to Access Claude

Claude is available through multiple interfaces, each designed for different use cases. Pick the one that fits your needs.

### 1. Web Interface (claude.ai)

The quickest way to start. Open [claude.ai](https://claude.ai) in any modern browser -- no installation required.

- **Best for**: Getting started, casual use, trying things out
- **Works on**: Any device with a web browser
- **Cost**: Free tier available

### 2. Desktop App (macOS and Windows)

A standalone application that lives on your computer, separate from your browser.

- **Best for**: Focused deep work, frequent use, MCP integrations
- **Works on**: macOS and Windows
- **Advantage**: Stays open as its own window, supports connecting to local tools via MCP (Model Context Protocol -- a way for Claude to interact with other software on your machine)

### 3. Mobile App (iOS and Android)

Claude in your pocket for quick questions and conversations on the go.

- **Best for**: Quick questions while away from your computer, voice input
- **Works on**: iPhone, iPad, Android phones and tablets
- **Advantage**: Syncs conversations with the web and desktop apps

### 4. Claude Code (CLI)

A terminal-based tool that lets developers use Claude directly in their coding workflow.

- **Best for**: Software developers who live in the terminal
- **Works on**: macOS, Linux, Windows (via WSL)
- **Advantage**: Claude can read your project files, run commands, and make code changes directly

### 5. API (console.anthropic.com)

A programming interface for building applications that use Claude under the hood.

- **Best for**: Developers building products powered by Claude
- **Works on**: Any programming environment
- **Advantage**: Full control over how Claude is used, pay-per-token pricing

**Recommendation for beginners**: Start with the **web interface** at claude.ai. It requires nothing but a browser and gives you access to all of Claude's core features.

## Setting Up Your Account

Follow these steps to create your Claude account:

1. Open your web browser and go to [claude.ai](https://claude.ai)
2. Click **Sign Up**
3. Choose a sign-up method:
   - **Email**: Enter your email address and create a password
   - **Google**: Sign in with your existing Google account
   - **Apple**: Sign in with your Apple ID
4. If you chose email, check your inbox for a verification message and click the link
5. Complete your profile by entering your name
6. You will land on the chat screen -- you are ready to go

The entire process takes about two minutes.

## Navigating the Interface

Once you are logged in, here is what you will see:

### The Chat Area

This is the large central area where your conversation happens. You type your messages in the text box at the bottom, and Claude's responses appear above. You can:

- Type or paste text
- Attach files (PDFs, images, code files, and more)
- Use the model selector to choose which version of Claude to use

### The Model Selector

Located near the text input area, this dropdown lets you switch between Claude models:

| Model | When to Select It |
|---|---|
| **Sonnet** | Default choice -- good for nearly everything |
| **Opus** | When you need deeper reasoning on a hard problem |
| **Haiku** | When you need a quick, simple answer |

On the free tier, you may not have access to all models. Upgrading to Pro unlocks full access.

### The Conversation Sidebar

On the left side of the screen, you will find your conversation history. Each conversation is saved automatically. You can:

- Click any past conversation to reopen it
- Search through your conversation history
- Organize conversations into **Projects** for related work
- Delete conversations you no longer need

### The New Chat Button

At the top of the sidebar, the **New Chat** button starts a fresh conversation. Remember: each new conversation is a clean slate. Claude will not remember anything from your previous chats unless you explicitly provide that context.

## Settings to Configure First

Before diving in, take a moment to set up a few things:

### Enable Artifacts

**Artifacts** are a feature that lets Claude create standalone content -- like code, documents, or visualizations -- in a separate panel next to the chat. To enable them, click your profile icon, go to **Settings**, and toggle Artifacts on.

### Set Up Your Profile

Your profile helps Claude tailor responses to you. Click your profile icon, go to **Settings**, and find **Profile** or **Custom Instructions**. Add your profession, what you use Claude for, and your preferred response style.

**Example profile**: "I am a marketing manager. I use Claude for writing emails, analyzing reports, and brainstorming campaign ideas. I prefer concise responses with bullet points."

### Try It Yourself

Complete these steps to get fully set up:

1. Go to [claude.ai](https://claude.ai) and create an account (if you have not already)

2. Once logged in, send your first message by copying and pasting this prompt:
   ```
   Hello! Tell me something interesting about the history of computing that most people don't know.
   ```

3. While you are there, explore the interface:
   - Try clicking the model selector to see which models are available
   - Open the sidebar and look at your conversation history
   - Check the settings and enable Artifacts if available

4. Try attaching a file (any PDF or image you have on hand) and ask:
   ```
   Can you describe what this file contains and summarize the key points?
   ```

## Key Takeaways

- The easiest way to start is the **web interface** at claude.ai -- no installation needed
- Five access methods exist: web, desktop app, mobile app, Claude Code (CLI), and the API
- The interface has four main areas: chat area, model selector, conversation sidebar, and new chat button
- Set up Artifacts and your profile early for a better experience
- Each conversation is a clean slate -- Claude does not carry context between chats by default

## Next Steps

Your account is set up and you know your way around. Now learn how to have effective conversations: [Your First Conversation -- The Basics](04-your-first-conversation.md).
