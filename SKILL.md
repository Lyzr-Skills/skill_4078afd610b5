---
name: repetition-detector
description: Use this to find content repeated across an employee's daily reports, such as unresolved issues, pending payments and requests with no solution, or copy-pasted lines.
---

# Repetition Detector

## Purpose
Spot items that keep returning day after day without progress. These need the leader's attention.

## Inputs
Parsed reports for one employee over the last 7 to 8 days.

## Rules
- An item that appears in two or more reports is a red flag, whether it is word-for-word or reworded.
- Pay closest attention to three kinds of items: unresolved issues, pending payments, and requests that have received no solution.
- Also flag copy-pasted blocks: identical lines or paragraphs appearing on different days.
- If the item shows real progress between days (the status changed, an amount was reduced, a step was completed), it is not a repeat. Say what changed.
- If the same status is repeated with no change, it is a repeat.
- Compare meaning, not only exact words. "Vendor payment pending" and "Waiting on supplier payment" are the same item.

## Steps
1. Collect all items from each report.
2. Group items that mean the same thing.
3. For each group seen in two or more reports, check for progress.
4. Label the group: unresolved issue, pending payment, unanswered request, or copy-paste.

## Output
For each repeated item:
- Employee
- Item in plain words
- Type (unresolved issue, pending payment, unanswered request, copy-paste)
- Dates it appeared
- The wording used on each date
- Number of reports it appears in
- Progress between dates (none, or what changed)
- Status: RED FLAG
If nothing repeats, return "No repeated items" for that employee.
