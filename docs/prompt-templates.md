# Prompt Template Library

> Ready-to-use prompt templates. Copy, customize the [bracketed] parts, and paste into Claude.

## Learning and Growth Templates

### The Progressive Overload (Intelligent Gym)

Master a topic through escalating difficulty. Great for interview prep or learning new domains.

```text
You are my learning coach for [TOPIC]. Work through 4 difficulty levels. Evaluate my response after each, correct mistakes, and advance me only when I demonstrate understanding.

Level 1 (Foundations): Ask a clear, definitional question.
Level 2 (Application): A scenario requiring me to apply the concept.
Level 3 (Analysis): Challenge me with trade-offs or edge cases.
Level 4 (Stress Test): Grill me as if defending this to a skeptical expert.

Begin with Level 1 now.
```

**What to expect:** An interactive quiz that escalates only when you are ready.

### The Triple-Pass Simplification

Break down jargon-heavy concepts into plain language. Works for any domain.

```text
Simplify [CONCEPT/PASSAGE] in three passes:

Pass 1: Explain as if I am a smart 10-year-old. No jargon.
Pass 2: Simplify further. Remove any remaining technical terms.
Pass 3: Distill into a single vivid analogy that captures the core idea.

Here is the concept: [PASTE THE CONCEPT OR JARGON-HEAVY TEXT]
```

**What to expect:** Three increasingly simple explanations, ending with a memorable analogy.

### The Knowledge Gap Closer

Identify and fill gaps in your understanding. Great for new roles or career transitions.

```text
I work as a [YOUR ROLE] and need competency in [FIELD/DOMAIN]. Level: [BEGINNER/INTERMEDIATE/ADVANCED].

1. List the 10 most important concepts someone in my role must understand.
2. For each, write a one-sentence explanation.
3. Ask me 5 diagnostic questions to find my weakest areas.

After I answer, create a prioritized study plan for my top 3 gaps.
```

**What to expect:** A structured assessment followed by a personalized study plan.

## Writing and Creation Templates

### The Style Matcher (Few-Shot)

Get Claude to write in your voice. Provide 2-3 samples of your existing writing.

```text
Match my writing style. Study these samples:

Sample 1: [PASTE 100-200 WORDS OF YOUR WRITING]
Sample 2: [PASTE 100-200 WORDS OF YOUR WRITING]

Using the same tone, sentence structure, and vocabulary, write [DESCRIBE WHAT YOU NEED].
```

**What to expect:** Output mirroring your voice. Point out specific differences if it sounds off.

### The Structured Draft

Get a first draft with clear constraints on format, tone, and length.

```text
Write a [CONTENT TYPE: blog post / email / proposal / report] about [TOPIC].

- Audience: [WHO WILL READ THIS]
- Tone: [formal / conversational / technical / persuasive]
- Length: [WORD COUNT OR PAGE COUNT]
- Format: [paragraphs / bullets / numbered list / sections with headers]
- Must include: [KEY POINTS TO COVER]
- Must avoid: [ANYTHING TO EXCLUDE]
```

**What to expect:** A draft that follows your constraints. Iterate from there.

### The Editor's Eye

Critique and improve your existing writing before you send it.

```text
Review this text as a skilled editor for [INTENDED AUDIENCE]. Evaluate clarity, conciseness, structure, tone, and impact.

Give specific line-level suggestions. Rewrite the weakest paragraph.

[PASTE YOUR WRITING]
```

**What to expect:** Actionable feedback with concrete rewrites, not generic praise.

## Strategy and Analysis Templates

### The Devil's Advocate

Stress-test a plan or decision. Claude attacks your reasoning from every angle.

```text
Act as a Devil's Advocate. Find every flaw, risk, and logical gap. Do not be polite.

My plan: [DESCRIBE YOUR PLAN IN 3-5 SENTENCES]

Analyze: assumptions I am taking for granted, risks and their severity, blind spots, better alternatives, and the realistic worst-case scenario.

After your critique, suggest the 3 most important changes I should make.
```

**What to expect:** A thorough, uncomfortable critique. If too gentle, say "Be harsher."

### The PRIME Mission Brief

For complex, high-stakes tasks needing thorough context and structured execution.

```text
Purpose: [SPECIFIC GOAL]
Research context: [BACKGROUND -- paste or describe relevant data/documents]
Interview step: Before generating the final output, tell me what patterns you see, what assumptions you are making, and what additional info would help. I will confirm before you proceed.
Mechanics: Format: [FORMAT] | Length: [LENGTH] | Audience: [EXPERTISE LEVEL]
Examples: [PASTE A REFERENCE SHOWING THE QUALITY/STYLE YOU WANT]
```

**What to expect:** Claude pauses to check alignment before producing the final output.

### The Pros/Cons Analyzer

Structured, balanced evaluation when weighing multiple options for a decision.

```text
I am deciding between these options for [DECISION CONTEXT]:

Option A: [DESCRIBE OPTION A]
Option B: [DESCRIBE OPTION B]
Option C: [DESCRIBE OPTION C, IF APPLICABLE]

For each: top 3 advantages, top 3 disadvantages, hidden risks, and best/worst-case outcomes.
Give a clear recommendation with reasoning.
```

**What to expect:** A balanced comparison followed by a direct recommendation.

## Development Templates

### The Spec-First Architect (Karpathy Layer 1)

Plan before coding. Get architecture approved before implementation to reduce expensive rewrites.

```text
I need to build [DESCRIBE THE FEATURE/SYSTEM]. Before writing code, create a spec:

1. Requirements: Functional and non-functional.
2. Architecture: Components and how they interact.
3. Data model: Key entities and relationships.
4. API surface: Main interfaces or endpoints.
5. Edge cases: Tricky scenarios to handle.
6. Tech choices: Recommended tools/frameworks and why.

Do NOT write implementation code. I want to approve the architecture first.
Context: [TECH STACK, EXISTING CODEBASE, CONSTRAINTS]
```

**What to expect:** A structured spec to review and refine before writing any code.

### The Code Reviewer

Review code for bugs, style, performance, and improvements.

```text
Review this code as a senior engineer. Be thorough and direct.

Language: [e.g., Python/FastAPI, TypeScript/React] | Purpose: [BRIEF DESCRIPTION]
Check for: bugs, security issues, performance, readability, best practices.
For each issue, show the problematic line and suggest a fix.

[PASTE YOUR CODE]
```

**What to expect:** A prioritized list of issues with specific fixes.

### The Debugger

Systematically debug an error with full context upfront.

```text
Help me debug this issue:

Error: [PASTE THE EXACT ERROR MESSAGE]
Language: [e.g., Python 3.11, Node 20]
Expected: [WHAT SHOULD HAPPEN] | Actual: [WHAT HAPPENS INSTEAD]
Already tried: [YOUR DEBUGGING ATTEMPTS]
Code: [PASTE CODE WITH SURROUNDING CONTEXT]

List most likely causes in order of probability with a specific fix for each.
```

**What to expect:** A ranked list of probable causes with targeted fixes.

### The Test Writer

Generate test cases for existing code with your testing framework and conventions.

```text
Write tests for this code using [FRAMEWORK: e.g., pytest, Jest, Go testing].

[PASTE THE CODE TO TEST]

Cover: happy path, edge cases (empty/boundary/max), error cases, and mock [EXTERNAL DEPENDENCIES].
Naming convention: [YOUR PATTERN, e.g., "test_should_[behavior]_when_[condition]"]
```

**What to expect:** A complete test file ready to drop into your project.

## Research Templates

### The Deep Dive

Comprehensive research on a topic, synthesized from multiple angles.

```text
Conduct a thorough analysis of [TOPIC]:

1. Overview: What is it and why does it matter?
2. Current state: Latest thinking or developments?
3. Key players: Important people, companies, or organizations?
4. Core tensions: Main debates or disagreements?
5. Practical implications: How does this affect [YOUR CONTEXT]?
6. Common misconceptions: What do most people get wrong?

Cite specific examples or case studies. Flag anything you are uncertain about.
```

**What to expect:** A structured briefing. For time-sensitive topics, combine with Claude's web search.

### The Comparison Matrix

Evaluate multiple tools, products, or approaches side by side across consistent dimensions.

```text
Compare [OPTION 1], [OPTION 2], [OPTION 3] for [USE CASE].

Evaluate across:
1. [DIMENSION 1: e.g., Ease of setup]
2. [DIMENSION 2: e.g., Scalability]
3. [DIMENSION 3: e.g., Cost]
4. [DIMENSION 4: e.g., Community/ecosystem]
5. [DIMENSION 5: e.g., Learning curve]

Rate each (strong / adequate / weak) with a brief assessment.
Then: best overall, best for [SCENARIO 1], best for [SCENARIO 2].
```

**What to expect:** A structured comparison for decision-making. Adjust dimensions to your priorities.
