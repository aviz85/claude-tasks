---
description: Re-prioritize all tasks using Eisenhower matrix
allowed-tools: Read, Edit
skills: priority-matrix
---

# Reprioritize Tasks

## First: Check the Clock
Current time: !`date "+%Y-%m-%d %H:%M:%S %Z"`

## Context
- Inbox: !`cat tasks/inbox.md 2>/dev/null`
- Today: !`cat tasks/today.md 2>/dev/null`
- Backlog: !`cat tasks/backlog.md 2>/dev/null`

## Instructions

1. **Gather all tasks** from inbox, today, and backlog

2. **Apply Eisenhower Matrix** to each task:
   - Q1 (Do First): Urgent + Important → `!high`
   - Q2 (Schedule): Important, Not Urgent → `!medium`
   - Q3 (Delegate): Urgent, Not Important → `!low`
   - Q4 (Eliminate): Not Urgent, Not Important → someday or delete

3. **Reorganize files**:
   - Move Q1 tasks to "Do First" section in backlog
   - Move Q2 tasks to "Schedule" section
   - Move Q3 tasks to "Delegate" section
   - Move Q4 tasks to someday.md or suggest deletion

4. **Update today.md**:
   - Ensure max 3 focus tasks
   - All should be Q1 priority

5. **Report changes**:
   - Tasks promoted (moved up in priority)
   - Tasks demoted (moved down)
   - Tasks suggested for elimination

## Output Format

```
## Reprioritization Complete

### Promoted (now higher priority)
- [Task] !low → !high (reason)

### Demoted (now lower priority)
- [Task] !high → !medium (reason)

### Suggested for Removal
- [Task] - hasn't moved in [N] days

### Current State
- Do First: [N] tasks
- Schedule: [N] tasks
- Delegate: [N] tasks
- Someday: [N] tasks
```
