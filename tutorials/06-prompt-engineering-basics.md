# Prompt Engineering Basics -- Getting Better Results

> **What you will learn:** The 5 elements of an effective prompt, with concrete before/after examples.
> **Prerequisites:** [Context and Memory](05-context-and-memory.md)
> **Time:** 15 minutes

## What Is Prompt Engineering?

"Prompt engineering" sounds technical, but it is really just **clear communication**. The better you explain what you want, the better Claude's output will be.

You would not walk up to a colleague and say "do the thing." You would say what you need, give them context, and describe the format you want. The same principle applies to Claude.

## The 5 Elements of a Good Prompt

### 1. Role -- Who should Claude be?

Setting a role gives Claude a perspective and expertise level to work from.

```text
You are a senior data analyst with 10 years of experience in e-commerce.
```

### 2. Task -- What exactly should Claude do?

Be specific about the action you want. "Help me" is vague. "Write," "analyze," "compare," "summarize," "debug" are specific.

```text
Analyze this sales data and identify the top 3 trends.
```

### 3. Context -- What does Claude need to know?

Paste relevant information, describe the situation, or upload files. More context = better results.

```text
Here is our Q3 sales data by region: [paste data]
We launched a new product in August in the West region.
```

### 4. Format -- How should the output look?

Tell Claude exactly what shape the answer should take.

```text
Present your findings as:
- A bullet-point summary (3-5 points)
- A markdown table comparing regions
- One paragraph with your recommendation
```

### 5. Constraints -- What are the boundaries?

Set limits on length, tone, complexity, or what to avoid.

```text
Keep the summary under 200 words.
Use language a non-technical manager would understand.
Do not include raw numbers -- use percentages and comparisons.
```

## Before and After: Real Examples

### Example 1: Writing an email

**Before (vague):**
```text
Write me an email about the meeting change.
```

**After (using all 5 elements):**
```text
You are a friendly project manager.

Write a professional email to my team (8 people) announcing that next
week's Wednesday standup is moving from 10am to 2pm due to a client
visit in the morning.

Keep it under 100 words. Friendly but professional tone.
Include a note asking people to update their calendars.
```

### Example 2: Debugging code

**Before (vague):**
```text
My code doesn't work. Help.
```

**After (using all 5 elements):**
```text
You are an experienced Python developer.

Debug this function that should return a sorted list of unique values,
but it returns an empty list instead.

Here's the code:
def get_unique_sorted(items):
    unique = set(items)
    sorted(unique)
    return list(unique)

Here's the error behavior: get_unique_sorted([3,1,2,1]) returns
[1,2,3] sometimes and [2,3,1] other times instead of always [1,2,3].

Explain the bug, show the fix, and explain why the fix works.
```

### Example 3: Research and analysis

**Before (vague):**
```text
Tell me about remote work.
```

**After (using all 5 elements):**
```text
You are a business strategy consultant.

Summarize the key arguments for and against fully remote work policies
for a mid-size software company (50-200 employees).

Consider: productivity, hiring, culture, cost, and employee retention.

Format as a comparison table with "For" and "Against" columns, followed
by a 3-sentence recommendation. Keep the total response under 300 words.
```

## The Iteration Principle

You do not need to get the perfect prompt on the first try. Treat it as a conversation:

1. **Start** with a reasonably specific prompt
2. **Evaluate** the response -- what is missing or off?
3. **Refine** by asking Claude to adjust: "Make it shorter," "Add more examples," "Use a more formal tone"
4. **Repeat** until the output matches what you need

This iterative approach is often faster than spending 10 minutes crafting the "perfect" initial prompt.

## Common Mistakes to Avoid

| Mistake | Why It Fails | Fix |
|---------|-------------|-----|
| Being too vague | Claude has to guess what you want | Add task, context, and format |
| Giving no examples | Claude has no reference point for your style | Include 1-2 examples of desired output |
| Asking too many things at once | Responses get unfocused | Break complex requests into steps |
| Not saying what format you want | Claude picks its own structure | Specify: bullet points, table, paragraph, code, etc. |
| Ignoring follow-up | First response is treated as final | Iterate -- ask for changes and refinements |

### Try It Yourself

**Exercise 1: Transform a vague prompt**

Take this vague prompt and rewrite it using all 5 elements:
```text
Help me with my presentation.
```

Then send both versions to Claude (the vague one first, then your improved one) and compare the responses.

**Exercise 2: Iterate on a response**

1. Ask Claude: "Explain how a computer works."
2. Then refine: "Explain that using an analogy a 10-year-old would understand."
3. Then refine again: "Now make it exactly 3 sentences."
4. Notice how each refinement gets you closer to what you want.

**Exercise 3: Format control**

Ask Claude the same question three ways:
1. "What are the benefits of exercise?" (no format specified)
2. "List the benefits of exercise as 5 bullet points."
3. "Create a table of the benefits of exercise with columns: Benefit, Physical Impact, Mental Impact."

Compare how format instructions change the output.

## Key Takeaways

- Prompt engineering is just clear communication -- Role, Task, Context, Format, Constraints
- Specific prompts get dramatically better results than vague ones
- You do not need the perfect prompt on the first try -- iterate
- Always specify the output format you want
- More context = better results (paste data, describe the situation, set the scene)

## Next Steps

Learn how to set up persistent context in [Projects and Knowledge](07-projects-and-knowledge.md), or jump ahead to [Advanced Prompting](09-advanced-prompting.md) for techniques like chain-of-thought and few-shot prompting.
