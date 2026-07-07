# Projects and Knowledge Bases

> **What you will learn:** How to create Claude Projects, upload documents, and use persistent context to get more accurate, grounded responses.
> **Prerequisites:** [Context and Memory](05-context-and-memory.md)
> **Time:** 10 minutes

## What Are Claude Projects?

In [Tutorial 05](05-context-and-memory.md), you learned that Claude forgets everything between conversations. **Projects** solve this problem.

A Claude Project is a workspace where you can:

- **Upload documents** that Claude references in every conversation within the project
- **Set custom instructions** that define Claude's behavior for that project
- **Keep conversations organized** by topic or domain

Think of a Project as giving Claude a specialized briefing folder before each conversation starts.

## Creating Your First Project

1. Open Claude (web or desktop app)
2. Click **"Projects"** in the sidebar (requires a Pro plan)
3. Click **"Create Project"**
4. Give it a name (e.g., "Work Reports" or "Learning Python")
5. Optionally add a description

That is it -- you now have a workspace you can keep coming back to.

## Uploading Documents (Knowledge Grounding)

The most powerful feature of Projects is uploading documents that Claude can reference. This is called **grounding** -- you are tethering Claude to real information instead of letting it guess.

### What you can upload

| File Type | Good For |
|-----------|----------|
| PDFs | Reports, papers, manuals, specifications |
| Text files | Notes, documentation, code |
| Code files | Source code for review, debugging, or learning |
| Images | Diagrams, screenshots, mockups |

### How to upload

1. Open your project
2. Click the **"Add content"** or **"Upload"** button in the project settings
3. Select files from your computer
4. Claude will now reference these documents in every conversation within this project

### What grounding does

Without grounding, Claude answers from its general training data -- broad but sometimes inaccurate for your specific situation.

With grounding, Claude references **your actual documents** and gives answers based on what is actually written there.

**Example without grounding:**
```text
You: What is our company's refund policy?
Claude: Typically, companies offer 30-day refund policies... [generic answer]
```

**Example with grounding (company policy PDF uploaded):**
```text
You: What is our company's refund policy?
Claude: According to your policy document, customers can request a full
refund within 14 days of purchase. After 14 days, a 15% restocking fee
applies. Digital products are non-refundable once downloaded. [specific answer]
```

## Setting Project Instructions

Project instructions act as a persistent system prompt -- they tell Claude how to behave in every conversation within that project.

Click **"Set instructions"** in your project settings and write rules like:

```text
You are a technical documentation specialist for our team.
Always reference the uploaded API documentation when answering questions.
Use markdown formatting in all responses.
If the answer is not in the uploaded documents, say "I don't see this
covered in the documentation" rather than guessing.
When providing code examples, use Python 3.11 syntax.
```

These instructions apply automatically to every new conversation in the project -- you do not need to repeat them.

## Organizing Projects by Domain

Create separate projects for different areas of your work or life. This keeps context clean and prevents Claude from mixing up information across domains.

| Project | What to Upload | Example Instructions |
|---------|---------------|---------------------|
| "Work - Q3 Reports" | Sales data, past reports | "Act as a business analyst. Match the tone of past reports." |
| "Learning Python" | Tutorial notes, your code exercises | "Act as a patient Python tutor. Explain concepts before showing code." |
| "Blog Writing" | Published posts, style notes | "Match the voice in my uploaded posts. Keep paragraphs under 4 sentences." |
| "Home Renovation" | Floor plans, contractor quotes | "Help me compare options and track decisions." |

## Best Practices

**Do upload:**
- Documents Claude needs to reference accurately
- Style guides or examples of your past work
- Technical specifications or requirements
- Data you want analyzed across multiple conversations

**Do not upload:**
- Sensitive credentials, passwords, or API keys
- Extremely large datasets (they eat into the context window)
- Frequently changing documents (you will need to re-upload when they change)

### Try It Yourself

**Exercise 1: Create a learning project**
1. Create a new project called "Learning [Topic]" (pick any topic you want to learn)
2. Set the project instructions to: "You are a patient tutor helping me learn [topic]. Start explanations from basics. Quiz me after each concept to check understanding."
3. Start a conversation and begin learning

**Exercise 2: Upload and query a document**
1. Find any PDF or text document you have (a report, an article, notes)
2. Upload it to a project
3. Ask Claude specific questions about the document
4. Notice how the answers reference your actual document content

## Key Takeaways

- Projects give Claude persistent context that survives across conversations
- Uploading documents **grounds** Claude in real information, reducing hallucination
- Project instructions define Claude's behavior automatically for every conversation in that project
- Separate projects for different domains keep context clean
- Do not upload sensitive credentials or frequently changing files

## Next Steps

Learn about visual and interactive output in [Using Artifacts](08-using-artifacts.md).
