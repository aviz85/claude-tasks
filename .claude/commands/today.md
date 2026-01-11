---
description: Show today's tasks and progress
allowed-tools: Read
---

# Today's Tasks

## First: Check the Clock
Current time: !`date "+%Y-%m-%d %H:%M:%S %Z"`

## Context
- Current date: !`date +%Y-%m-%d`
- Today file: !`cat tasks/today.md 2>/dev/null || echo "No tasks for today yet"`

## Instructions

1. Read and display the contents of `tasks/today.md`
2. Show a summary:
   - Number of focus tasks (max 3)
   - Total estimated time
   - Completed vs remaining
3. If today.md is empty or missing, suggest running `/standup`

## Output Format

```
## Today - [DATE]

### Focus Tasks
[List focus tasks with status]

### Progress
- Completed: X/Y tasks
- Remaining time: ~Xh

### Suggestions
[If tasks are done, suggest what's next]
```
