# Claude for Coding

> **What you will learn:** How to use Claude for writing, debugging, reviewing, and testing code, plus an introduction to Claude Code (the CLI tool).
> **Prerequisites:** [Prompt Engineering Basics](06-prompt-engineering-basics.md)
> **Time:** 15 minutes

## What Claude Can Do with Code

Claude is a strong coding assistant. It can:

- **Write code** from a description of what you need
- **Debug errors** when you paste the error message and relevant code
- **Explain code** you do not understand
- **Refactor** existing code for clarity or performance
- **Review** your code for bugs, security issues, and style
- **Write tests** for existing functions
- **Convert** code between languages

## Writing Code from a Description

The key to getting good code from Claude is describing **what** the code should do, not **how** to write it. Include:

- The programming language
- What the function/program should accomplish
- Input/output expectations
- Any constraints or edge cases

```text
Write a Python function called `parse_csv_dates` that:
- Takes a CSV file path as input
- Reads the file and finds all columns that contain date values
- Converts those columns from string format to datetime objects
- Returns a pandas DataFrame with the converted dates
- Handles the formats: YYYY-MM-DD, MM/DD/YYYY, and DD-Mon-YYYY
- Raises a ValueError if the file does not exist
```

## Debugging: The Most Valuable Use Case

Debugging is where Claude saves the most time. Provide three things:

1. **The code** (relevant function or section, not the entire codebase)
2. **The error message** (full traceback or error output)
3. **What you expected** vs what happened

```text
This Python function should return the average of a list of numbers,
but it returns 0 for the input [1, 2, 3, 4, 5].

def calculate_average(numbers):
    total = 0
    for n in numbers:
        total + n
    return total / len(numbers)

Error: No error thrown, but it returns 0.0 instead of 3.0.
What am I missing?
```

Claude will identify that `total + n` does not modify `total` -- it should be `total += n`.

## Code Review

Paste your code and ask for a specific type of review:

```text
Review this Express.js route handler for:
1. Security vulnerabilities (especially injection risks)
2. Error handling gaps
3. Performance concerns

[paste your code]
```

For a general review:
```text
Review this code. Focus on bugs first, then suggest improvements
for readability and maintainability.

[paste your code]
```

## Writing Tests

Claude can generate test cases for existing code:

```text
Write pytest tests for this function. Include:
- Happy path tests
- Edge cases (empty input, single element, very large input)
- Error cases (invalid types, None input)

def find_duplicates(items: list) -> list:
    seen = set()
    duplicates = set()
    for item in items:
        if item in seen:
            duplicates.add(item)
        seen.add(item)
    return sorted(list(duplicates))
```

## The Spec-First Approach

For larger projects, do not jump straight to code. Use the **Karpathy Method** (covered in the [Frameworks guide](../docs/frameworks-and-strategies.md)):

1. **Describe what you want to build** in plain language
2. **Ask Claude to create an architecture/spec** -- review and approve it
3. **Then ask Claude to implement** based on the approved spec

```text
I want to build a command-line expense tracker in Python.

Before writing any code, create a specification document that covers:
- Core features and user commands
- Data storage approach
- Input validation rules
- File structure

Do not write code yet. Let me approve the spec first.
```

## Introduction to Claude Code

**Claude Code** is a terminal-based tool that brings Claude directly into your development environment. Instead of copy-pasting code into a web chat, Claude Code can:

- Read and edit files in your project directly
- Run commands and see the output
- Navigate your codebase to understand context
- Make changes across multiple files
- Run tests and fix issues in a loop

### Basic usage

```bash
# Install
npm install -g @anthropic-ai/claude-code

# Start in your project directory
cd my-project
claude

# Ask Claude to do something
> Fix the failing test in tests/test_auth.py
> Add input validation to the signup form
> Explain what the process_payment function does
```

Claude Code is especially powerful for tasks that span multiple files or require understanding the full project context.

## Tips for Better Code Assistance

| Tip | Why It Helps |
|-----|-------------|
| Specify the language and version | "Python 3.11" vs "Python" avoids outdated syntax |
| Paste relevant imports and types | Claude needs to know what libraries you are using |
| Include the full error traceback | Partial errors lead to guesses |
| Describe the broader context | "This is part of a REST API" helps Claude make consistent choices |
| Ask Claude to explain its changes | "Explain why you changed line 15" builds your understanding |

### Try It Yourself

**Exercise 1: Debug a function**

Send this to Claude and see if it can find and fix the bug:
```text
This function should reverse a string, but it throws an error:

def reverse_string(text):
    result = ""
    for i in range(len(text), 0):
        result += text[i]
    return result

Error: returns an empty string for any input.
```

**Exercise 2: Generate tests**

Take a simple function you have written (or use the `find_duplicates` example above) and ask Claude to write comprehensive tests for it.

**Exercise 3: Spec-first project**

Ask Claude to spec out a small project (a to-do list, a quiz app, a note-taking tool) before writing any code. Review the spec, give feedback, then ask for implementation.

## Key Takeaways

- Always provide the language, error messages, and expected behavior when asking for code help
- Debugging is Claude's highest-value coding use case -- paste the error, code, and expectation
- Use the spec-first approach for anything beyond a single function
- Claude Code brings AI assistance directly into your terminal and codebase
- Always test Claude's code -- it can contain subtle bugs

## Next Steps

Learn how Claude can help with writing in [Claude for Writing](11-claude-for-writing.md).
