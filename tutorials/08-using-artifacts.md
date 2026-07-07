# Using Artifacts -- Visual and Interactive Output

> **What you will learn:** What Artifacts are, the types of content they can render, and how to use them for visual, interactive, and code-based output.
> **Prerequisites:** [Your First Conversation](04-your-first-conversation.md)
> **Time:** 10 minutes

## What Are Artifacts?

Normally, Claude responds with text in the chat window. **Artifacts** are a special output panel that appears alongside the chat, rendering content visually -- code with syntax highlighting, HTML pages, diagrams, documents, and even interactive applications.

Think of it as a built-in preview window. Instead of just getting code as text, you can see the result rendered live.

## Types of Artifacts

| Artifact Type | What It Renders | Example Use |
|---------------|----------------|-------------|
| **Code** | Syntax-highlighted source code | Python scripts, JavaScript functions |
| **Documents** | Formatted text with headings and styles | Reports, proposals, articles |
| **HTML/CSS/JS** | Live web pages and interactive apps | Calculators, forms, landing pages |
| **SVG** | Vector graphics and illustrations | Icons, logos, simple diagrams |
| **Mermaid diagrams** | Flowcharts, sequence diagrams, org charts | Process flows, system architecture |
| **React components** | Interactive UI components | Dashboards, data visualizers, tools |

## How to Get Artifacts

Claude creates artifacts automatically when the content is substantial enough and visual rendering would be helpful. You can also ask explicitly:

```text
Create an HTML page with a tip calculator that splits the bill
between multiple people.
```

```text
Draw a Mermaid flowchart showing the user signup process:
1. User enters email
2. System sends verification email
3. User clicks link
4. User sets password
5. Account is created
```

```text
Write a Python script that reads a CSV file and prints a summary
of each column. Show it as an artifact.
```

## Working with Artifacts

### Editing and iterating

Once Claude creates an artifact, you can ask for changes in the chat:

- "Change the background color to dark blue"
- "Add a reset button"
- "Make the chart use a bar graph instead of a line graph"
- "Add error handling for empty input"

Claude will update the artifact in place, so you can see changes immediately.

### Copying and downloading

- **Copy code**: Click the copy button on code artifacts to grab the source
- **Download**: Some artifacts can be downloaded directly
- **Preview**: HTML and React artifacts render live -- you can interact with them right in the panel

### Version history

Claude keeps the history of artifact changes within a conversation. You can ask Claude to "go back to the previous version" if a change did not work out.

## Practical Examples

### Example 1: A quick web tool

```text
Create an interactive HTML page with a Pomodoro timer.
It should have:
- A 25-minute countdown display
- Start, pause, and reset buttons
- A clean, minimal design with a dark theme
```

### Example 2: A process diagram

```text
Create a Mermaid diagram showing how a customer support ticket flows:
Customer submits ticket → Auto-assigned to team → Agent reviews →
Agent responds → Customer confirms resolved OR escalates →
Ticket closed
```

### Example 3: A data dashboard

```text
Create a React component that displays a simple dashboard with:
- 3 stat cards at the top (Total Users: 1,234, Active Today: 567, New This Week: 89)
- A bar chart below showing daily active users for the past 7 days
Use sample data. Make it look clean and modern.
```

## When Artifacts Work Best

**Great for:**
- Prototyping web pages and UI components quickly
- Visualizing processes, flows, and system architecture
- Creating interactive tools (calculators, converters, timers)
- Rendering formatted documents and reports
- Exploring code with syntax highlighting

**Limitations:**
- Artifacts run in a sandboxed environment -- they cannot access your filesystem or external APIs
- Complex applications with many files are better built outside of Artifacts
- Artifacts exist within the conversation -- they are not saved permanently unless you copy the code

### Try It Yourself

**Exercise 1: Create an interactive tool**

Ask Claude:
```text
Create an HTML page with a unit converter. It should convert between
kilometers and miles, with an input field and a convert button.
Make it look clean.
```

Interact with the artifact -- try converting some values.

**Exercise 2: Create a diagram**

Ask Claude:
```text
Create a Mermaid flowchart of my morning routine:
Wake up → Check phone → Make coffee → Shower → Get dressed → Leave house
Add a decision diamond after "Check phone": if urgent emails, go to
"Handle emails" before "Make coffee"
```

**Exercise 3: Iterate on a design**

1. Ask Claude to create a simple personal landing page in HTML
2. Then ask: "Change the color scheme to dark mode"
3. Then ask: "Add a section listing 3 of my skills"
4. Notice how the artifact evolves with each instruction

## Key Takeaways

- Artifacts render visual content alongside the chat -- code, HTML, diagrams, React components
- You can iterate on artifacts by asking for changes in the chat
- Artifacts are great for prototyping, diagrams, and interactive tools
- They run in a sandbox and cannot access your files or external services
- Ask explicitly for an artifact if Claude does not create one automatically

## Next Steps

Level up your prompting with advanced techniques in [Advanced Prompting](09-advanced-prompting.md).
