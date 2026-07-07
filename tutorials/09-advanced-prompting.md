# Advanced Prompting Techniques

> **What you will learn:** Powerful prompting methods -- few-shot, chain of thought, role prompting, and structured output -- with copy-paste examples.
> **Prerequisites:** [Prompt Engineering Basics](06-prompt-engineering-basics.md)
> **Time:** 15 minutes

## Beyond the Basics

In [Tutorial 06](06-prompt-engineering-basics.md), you learned the 5 elements of a good prompt. This tutorial builds on that foundation with techniques that significantly improve Claude's performance on complex tasks.

## Technique 1: One-Shot Prompting

Provide a single example of the output you want. Claude matches the pattern.

```text
Convert customer feedback into structured action items.

Example:
Feedback: "The checkout process takes too long and I couldn't find where to apply my coupon code."
Action items:
- Investigate checkout flow for performance bottlenecks
- Improve coupon code field visibility on checkout page

Now do the same for this feedback:
"Your mobile app crashes when I try to upload a photo, and the text is too small to read on my phone."
```

**When to use:** When you want a specific output structure and one example makes the pattern clear.

## Technique 2: Few-Shot Prompting

Provide 2-3 examples to establish a strong pattern. More examples = more consistent output.

```text
Classify these support tickets by priority.

Examples:
Ticket: "Can't log in, password reset email never arrives"
Priority: HIGH - Account access blocked
Category: Authentication

Ticket: "The font on the settings page looks different than before"
Priority: LOW - Visual inconsistency
Category: UI

Ticket: "All customer data showing as $0.00 in reports since Monday"
Priority: CRITICAL - Data integrity issue
Category: Reporting

Now classify:
Ticket: "Export to PDF button produces a blank document"
```

**When to use:** When you need consistent formatting, classification, or tone across multiple inputs. The more examples you provide, the more reliably Claude follows the pattern.

**Pro tip:** After providing examples, ask Claude: "Before you begin, explain the pattern you see in my examples." This ensures Claude understood what you intended, not just what it assumed.

## Technique 3: Chain of Thought

Ask Claude to think step by step. This is the single most effective technique for improving accuracy on reasoning tasks.

```text
A store has a 25% off sale. A customer has a $10 coupon that applies
after the discount. The item costs $80. The customer also has to pay
8% sales tax on the final price.

Think step by step. Show your work for each step before giving
the final answer.
```

Without chain of thought, Claude might jump to a wrong answer. With it, Claude works through each step visibly, catching errors along the way.

**When to use:** Math, logic problems, multi-step analysis, debugging, any task where the reasoning process matters.

**Key phrases that trigger deeper reasoning:**
- "Think step by step"
- "Show your reasoning"
- "Walk me through your thought process"
- "Before answering, consider each factor"

## Technique 4: Role Prompting

Assigning a specific expert role changes how Claude approaches a problem -- the vocabulary it uses, the concerns it raises, and the depth of its analysis.

```text
You are a senior security engineer reviewing a web application.
Analyze this login form code and identify any security vulnerabilities.
Focus on OWASP Top 10 risks.
[paste code]
```

Different roles produce different results on the same input:

| Role | Focus |
|------|-------|
| "You are a UX designer" | Usability, accessibility, user flow |
| "You are a performance engineer" | Speed, memory usage, scalability |
| "You are a technical writer" | Clarity, completeness, readability |
| "You are a skeptical investor" | Risks, costs, market competition |

**When to use:** Whenever you want a specific expert perspective on your work.

## Technique 5: Structured Output

Tell Claude exactly what structure to return. This is especially useful when you need to process the output programmatically or compare results.

```text
Analyze this product review and return your analysis in this exact format:

Sentiment: [positive/negative/mixed]
Key praise: [bullet points]
Key complaints: [bullet points]
Suggested improvements: [numbered list]
Overall rating: [1-5]

Review: "The headphones sound amazing and the noise cancellation is
top-notch. However, they're uncomfortable after 2 hours and the case
feels cheap. Battery life is great though."
```

You can also request JSON, CSV, markdown tables, or any structured format.

## Technique 6: The "Explain Back" Technique

Before Claude executes a complex task, ask it to confirm its understanding.

```text
I need you to reorganize our product catalog. Here are the current
categories and the rules for the new structure: [paste details]

Before you start reorganizing, summarize:
1. What you understand the current structure to be
2. What rules you will follow for the reorganization
3. Any edge cases you see that I should clarify
```

This catches misunderstandings before Claude does a large amount of work in the wrong direction.

**When to use:** Complex tasks, high-stakes output, or when your instructions might be ambiguous.

## Combining Techniques

The real power comes from combining methods. Here is an example using role + chain of thought + structured output:

```text
You are a financial analyst reviewing a startup's pitch deck.

Analyze this business model step by step:
1. First, identify the revenue streams
2. Then, evaluate each stream's scalability
3. Finally, identify the biggest risk

[paste business model description]

Format your response as:
## Revenue Streams
[numbered list with brief description]

## Scalability Assessment
[table with columns: Stream, Scalability (High/Med/Low), Reasoning]

## Top Risk
[one paragraph]
```

### Try It Yourself

**Exercise 1: Chain of thought comparison**

Send this prompt twice -- once without and once with "think step by step":
```text
I have 3 boxes. Box A is to the left of Box B. Box C is to the right
of Box A but to the left of Box B. What is the order of the boxes
from left to right?
```

Compare the accuracy and reasoning.

**Exercise 2: Few-shot classification**

Create your own few-shot prompt to classify emails as "Action Required," "FYI Only," or "Spam." Provide 3 examples, then test it with a new email you write.

**Exercise 3: Role switching**

Take the same piece of text (a paragraph from an article or your own writing) and analyze it with two different roles:
1. "You are a writing coach focused on clarity"
2. "You are a fact-checker focused on accuracy"

Notice how the role changes what Claude focuses on.

## Key Takeaways

- **One-shot/few-shot**: Provide examples to establish patterns for consistent output
- **Chain of thought**: "Think step by step" dramatically improves reasoning accuracy
- **Role prompting**: Different expert roles produce different (useful) perspectives
- **Structured output**: Specify the exact format you want to get predictable results
- **Explain back**: Have Claude confirm its understanding before executing complex tasks
- Combine techniques for the best results on complex tasks

## Next Steps

Apply these techniques to specific domains: [Claude for Coding](10-claude-for-coding.md), [Claude for Writing](11-claude-for-writing.md), or [Claude for Research](12-claude-for-research.md).
