# Claude for Writing

> **What you will learn:** How to use Claude for drafting, editing, style matching, and brainstorming across different types of writing.
> **Prerequisites:** [Prompt Engineering Basics](06-prompt-engineering-basics.md)
> **Time:** 10 minutes

## How Claude Helps with Writing

Claude is not a replacement for your voice -- it is a tool that handles the mechanical parts of writing so you can focus on the ideas. Use it to:

- **Draft** when you are staring at a blank page
- **Edit** writing you have already done
- **Match** a specific tone or style
- **Brainstorm** ideas and outlines before you write
- **Rewrite** content for a different audience

## Getting Past the Blank Page

The hardest part of writing is starting. Let Claude create a rough draft that you can shape.

```text
Write a first draft of a 300-word blog post about why small businesses
should invest in cybersecurity.

Target audience: non-technical small business owners.
Tone: conversational, not scary. Focus on practical steps, not fear.
Include a real-world analogy to make the concept relatable.
```

**Important:** Treat Claude's draft as raw material, not a finished product. Your job is to edit, reshape, and inject your own perspective.

## Editing Your Own Writing

Paste your existing writing and ask for specific types of feedback:

```text
Edit this paragraph for clarity and conciseness. Keep my voice but
remove any redundant phrases or unclear sentences. Explain each
change you make.

[paste your paragraph]
```

For more targeted editing:

```text
Review this email for:
1. Tone -- is it professional but warm?
2. Clarity -- will a non-technical reader understand it?
3. Length -- can anything be cut without losing meaning?

Suggest specific edits with brief explanations.

[paste your email]
```

## Matching Your Style

Claude can learn your writing style from examples. This is the **few-shot** technique applied to writing.

```text
Here are 3 samples of my writing:

Sample 1:
[paste a paragraph of your writing]

Sample 2:
[paste another paragraph]

Sample 3:
[paste another paragraph]

Analyze my writing style. Identify patterns in:
- Sentence length and structure
- Vocabulary level
- Tone and formality
- How I use transitions
- Any distinctive habits

Then use this style to write a 200-word introduction for an article
about remote team management.
```

**Pro tip:** Ask Claude to describe the patterns it found before writing. This "explain back" step ensures Claude actually captured your style, not a generic approximation.

## Brainstorming and Outlining

Before writing, use Claude to explore ideas:

```text
I want to write an article about the future of electric vehicles.
Give me 10 possible angles I could take, ranging from technical
to human interest. For each angle, include a one-line hook that
would grab a reader's attention.
```

Then turn a chosen angle into a structure:

```text
I like angle #4 (the impact on rural communities). Create a detailed
outline with:
- A compelling introduction approach
- 4-5 main sections with key points for each
- Ideas for data or examples I should include
- A strong closing that ties back to the introduction
```

## Rewriting for Different Audiences

The same information needs different presentation for different readers:

```text
Here is a technical explanation of our new API rate limiting feature:
[paste technical text]

Rewrite this for three audiences:
1. A CEO who wants to know the business impact (3 sentences)
2. A developer who needs to update their integration (1 paragraph with specifics)
3. A support agent who will explain it to customers (friendly, non-technical, 1 paragraph)
```

## Writing Types Where Claude Excels

| Writing Task | How to Prompt |
|-------------|--------------|
| Professional emails | Specify recipient, purpose, tone, and length |
| Documentation | Provide the code/product and specify the audience's technical level |
| Meeting summaries | Paste raw notes and ask for structured summary with action items |
| Social media posts | Specify platform, audience, character limit, and call to action |
| Reports | Provide data/findings and specify format (executive summary, full report) |
| Cover letters | Provide the job description and your experience highlights |

### Try It Yourself

**Exercise 1: Edit and improve**

Write a paragraph about any topic. Then ask Claude:
```text
Edit this for clarity and impact. For each change you make, explain
why in brackets.

[paste your paragraph]
```

**Exercise 2: Style matching**

Find 2-3 paragraphs you have written previously (emails, posts, notes). Ask Claude to analyze your style and then write something new in that style. Evaluate how close it gets.

**Exercise 3: Audience adaptation**

Pick a topic you know well. Ask Claude to explain it for three different audiences: a child, a peer, and an executive.

## Key Takeaways

- Use Claude for the mechanical parts of writing (drafting, editing, formatting) while you supply the ideas and voice
- Treat AI drafts as raw material to edit, not finished products
- Few-shot style matching works: provide 2-3 samples and ask Claude to analyze the pattern
- Always ask Claude to "explain back" the style or intent before it writes
- Rewriting for different audiences is one of Claude's strongest writing capabilities

## Next Steps

Learn how to use Claude for analysis and research in [Claude for Research](12-claude-for-research.md).
