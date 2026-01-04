---
description: Process inbox items using GTD methodology
allowed-tools: Read, Edit
skills: task-parsing, priority-matrix, time-estimation
---

# Process Inbox

## Context
- Inbox contents: !`cat tasks/inbox.md 2>/dev/null`
- Today's capacity: !`grep -c "\- \[ \]" tasks/today.md 2>/dev/null || echo 0` tasks already planned
- Backlog size: !`grep -c "\- \[ \]" tasks/backlog.md 2>/dev/null || echo 0` tasks

## GTD Processing Flow

For each inbox item, ask:

```
1. Is it actionable?
   ├── No → Trash it or → Someday/Maybe
   └── Yes ↓

2. What's the next action?
   └── Define specific next step ↓

3. Will it take less than 2 minutes?
   ├── Yes → DO IT NOW
   └── No ↓

4. Am I the right person?
   ├── No → Delegate (note who)
   └── Yes ↓

5. Does it have a specific deadline?
   ├── Yes → Schedule it (with date)
   └── No → Add to backlog with priority
```

## Instructions

1. Read each item in inbox
2. Apply GTD flow above
3. For each item, decide:
   - **Delete**: Not needed
   - **Someday**: `tasks/someday.md`
   - **Today**: `tasks/today.md` (if urgent and important)
   - **Backlog**: `tasks/backlog.md` (with priority)
   - **Project**: `projects/[name]/tasks.md`
4. Remove processed items from inbox
5. Report what was done

## Output Format

```
## Inbox Processing Complete

### Quick Actions (done now)
- [Task] - completed

### Added to Today
- [Task] !high - urgent deadline

### Added to Backlog
- [Task] !medium → Schedule section
- [Task] !low → Delegate section

### Moved to Someday
- [Task] - not actionable now

### Deleted
- [Task] - no longer relevant

Inbox is now empty!
```
