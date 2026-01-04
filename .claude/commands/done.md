---
description: Mark a task as complete
argument-hint: <task description or keyword>
allowed-tools: Read, Edit
---

# Mark Task Complete

Mark this task as done: $ARGUMENTS

## Instructions

1. Search for the task in these files (in order):
   - `tasks/today.md`
   - `tasks/inbox.md`
   - `tasks/backlog.md`
   - `projects/*/tasks.md`

2. Find the task matching "$ARGUMENTS" (fuzzy match on keywords)

3. Mark it complete:
   - Change `- [ ]` to `- [x]`
   - If in today.md, move to "## Completed" section

4. Log completion:
   - Create/update `logs/daily/[DATE].md`
   - Add entry: `- [TIME] Completed: [task]`

5. Confirm completion and suggest next task

## Archive Rule

At end of day, completed tasks from today.md should be moved to:
`tasks/archive/[DATE].md`

## Example

Input: `/done login bug`
Action: Finds "Fix login bug" in today.md, marks [x], logs it
Output: "Marked complete: Fix login bug @work. 2 tasks remaining today."
