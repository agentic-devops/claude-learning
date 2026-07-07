# Claude for Research and Analysis

> **What you will learn:** How to use Claude for summarization, data analysis, adversarial critique, and deep research.
> **Prerequisites:** [Advanced Prompting](09-advanced-prompting.md)
> **Time:** 10 minutes

## What Claude Can Analyze

Claude is strong at processing and reasoning about information you provide:

- **Summarize** long documents, articles, or meeting notes
- **Compare** options across multiple dimensions
- **Find patterns** in data you paste in
- **Critique** plans and strategies to find weaknesses
- **Synthesize** information from multiple sources into a coherent view

## Summarization

Paste a long document and ask for a structured summary:

```text
Summarize this article in 3 levels:
1. One sentence (the core takeaway)
2. Three bullet points (key supporting points)
3. One paragraph (detailed summary)

[paste article text]
```

For meeting notes:
```text
Here are the raw notes from our team meeting:

[paste notes]

Create a structured summary with:
- Key decisions made
- Action items (with who is responsible, if mentioned)
- Open questions that still need answers
- Topics to follow up on
```

## Comparison and Evaluation

Claude can systematically compare options when you provide the criteria:

```text
I'm choosing between three project management tools for a 15-person
engineering team. Here is what I know about each:

Tool A: [paste details]
Tool B: [paste details]
Tool C: [paste details]

Compare them across these dimensions:
- Ease of onboarding for the team
- Integration with GitHub and Slack
- Pricing for our team size
- Reporting capabilities

Format as a comparison table, then give a recommendation with reasoning.
```

## The Devil's Advocate: Adversarial Critique

One of the most valuable uses of Claude is attacking your own ideas before someone else does. This technique comes from the frameworks covered in the [reference guide](../docs/frameworks-and-strategies.md).

```text
Here is my plan for launching a new product:

[paste your plan]

Act as a Devil's Advocate. Your job is to find every weakness,
assumption, and risk in this plan. Be ruthless but specific.
For each flaw you identify:
1. State the problem clearly
2. Explain why it is a risk
3. Suggest how to mitigate it
```

### When to use adversarial critique

- Before presenting a plan to stakeholders
- Before making a significant investment of time or money
- When you suspect your plan might have blind spots
- When you need to prepare for tough questions

## Data Analysis

Claude can reason about data you paste into the conversation:

```text
Here are our monthly sales numbers for the past 12 months:

| Month | Revenue | New Customers | Churn Rate |
|-------|---------|--------------|------------|
| Jan   | $45,000 | 120          | 3.2%       |
| Feb   | $48,000 | 135          | 2.8%       |
| ...   | ...     | ...          | ...        |

Analyze this data:
1. Identify the most significant trends
2. Flag any anomalies or concerns
3. What would you investigate further based on this data?
4. Present 3 actionable recommendations
```

**Important limitation:** Claude reasons about data but does not perform statistical modeling. For complex quantitative analysis, use Claude to write the analysis code (Python/pandas/R) and then run it yourself.

## Deep Research Mode

Claude's **Deep Research** feature goes beyond a single conversation turn. When activated, it:

1. Breaks your question into sub-queries
2. Searches multiple web sources
3. Cross-references findings
4. Synthesizes a comprehensive answer with citations

```text
Research the current state of battery recycling technology.
Cover:
- Major companies and their approaches
- Current recycling rates vs production volume
- Regulatory landscape in the US and EU
- Emerging technologies in the next 3-5 years

Provide sources for all claims.
```

**When to use Deep Research:** For questions that require current information from multiple sources -- market analysis, technology landscape reviews, regulatory overviews, or competitive research.

**Note:** Deep Research is available on Pro plans and uses extended processing time.

## Building a Research Workflow

For thorough research, combine techniques in sequence:

1. **Start broad:** Ask Claude to outline the key areas of a topic
2. **Go deep:** Pick the most relevant areas and ask for detailed analysis
3. **Challenge:** Use the Devil's Advocate technique on your conclusions
4. **Synthesize:** Ask Claude to combine everything into a final summary

```text
Step 1: "What are the 5 key factors I should consider when evaluating
a move to microservices architecture?"

Step 2: "Let's go deeper on factor #3 (data management). What are
the specific challenges and common solutions?"

Step 3: "Play Devil's Advocate -- what are the strongest arguments
against microservices for a team of our size (8 developers)?"

Step 4: "Based on everything we've discussed, write a 1-page
recommendation memo for my CTO."
```

### Try It Yourself

**Exercise 1: Structured summarization**

Find a long article online (at least 1,000 words). Paste it into Claude and ask for the 3-level summary (one sentence, three bullets, one paragraph).

**Exercise 2: Devil's Advocate**

Describe a decision you are currently considering (it can be professional or personal). Ask Claude to act as a Devil's Advocate and find the weaknesses in your plan.

**Exercise 3: Comparison matrix**

Think of 2-3 options you are evaluating for something (tools, approaches, products). Ask Claude to build a comparison table across 4-5 dimensions you care about.

## Key Takeaways

- Provide the actual text or data for Claude to analyze -- do not ask it to research from memory alone
- Use structured summary requests (1 sentence, 3 bullets, 1 paragraph) for consistent results
- The Devil's Advocate technique is one of the most valuable uses of Claude for decision-making
- Deep Research mode searches the web and synthesizes from multiple sources
- For data analysis, Claude reasons well about the data but complex statistics should be done in code
- Build multi-step research workflows: broad overview, deep dives, challenge, synthesize

## Next Steps

Learn how to extend Claude's capabilities with external tools in [MCP and Integrations](13-mcp-and-integrations.md).
