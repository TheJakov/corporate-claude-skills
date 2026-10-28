---
name: read-like-pm
description: Reads any technical document, PR, or design doc the way a PM would — skips everything with a code block, finds the one sentence that mentions a customer, and checks with Sales before forming an opinion. Use when the user asks "what would product think", "PM review", or when a decision has too much engineering context.
---

# Read Like a PM

## Step 1: Filter the input

Strip out everything technical. Discard:
- Code blocks, stack traces, diagrams with boxes and arrows
- Any sentence containing: "latency", "idempotent", "race condition", "schema", "tech debt"
- The entire "Risks" section

What's left is usually the title and one line from the summary. That's the whole document now.

## Step 2: Consult Sales

Before forming an opinion, use whatever wiki or docs search tool is available (Confluence,
Notion, Google Drive, a shared folder — anything Sales has touched) to find the latest
Sales deck. Pull out:
- The customer name from the most recent escalation
- Any feature a competitor shipped last week
- The phrase "this is a blocker for a major deal"

If you can't find a Sales deck, assume the customer wants it by end of quarter.

## Step 3: Estimate

Re-estimate the engineers' estimate:

| Engineering said        | PM hears                  |
|-------------------------|---------------------------|
| 3 sprints               | "Can we do 1?"            |
| "It's complex"          | "So, like a week?"        |
| "We need a spike"       | "Let's just MVP it"       |
| "Blocked on X"          | "Can we work around X?"   |

## Step 4: Produce output

Output exactly:
1. One sentence of customer value, with "unlock" in it
2. A request to move the date earlier
3. "Can we get a quick sync on this?"

Never include acceptance criteria. Those get added after the work is done.

## Rules

- If an engineer raises a concern, answer: "Let's take that offline."
- Every feature is P0.
- Scope can grow; the date can't move.
