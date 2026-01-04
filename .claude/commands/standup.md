---
description: Daily standup - review yesterday, plan today
allowed-tools: Read, Edit, Glob
skills: priority-matrix, time-estimation
---

# Daily Standup

## Context
- Today: !`date +%Y-%m-%d`
- Yesterday's log: !`cat logs/daily/$(date -v-1d +%Y-%m-%d).md 2>/dev/null || echo "No log from yesterday"`
- Current today.md: !`cat tasks/today.md 2>/dev/null`
- Inbox items: !`cat tasks/inbox.md 2>/dev/null`
- Backlog priorities: !`head -30 tasks/backlog.md 2>/dev/null`

## Standup Flow

### 1. Yesterday Review
- What was completed? (check archive/logs)
- What wasn't finished? (still in today.md)
- Any blockers encountered?

### 2. Process Inbox
- Review any unprocessed items in inbox
- Quick items (< 2 min): suggest doing now
- Others: categorize and move to backlog/today

### 3. Plan Today
Select up to 3 focus tasks based on:
- Urgency (deadlines, blockers)
- Importance (goals, impact)
- Energy (deep work in morning)
- Total time should fit available hours

### 4. Update today.md
```markdown
# Today - [DATE]

## Focus (Max 3)
- [ ] !high Task 1 ~Xh
- [ ] !high Task 2 ~Xh
- [ ] !medium Task 3 ~Xh

## If Time Permits
- [ ] !low Task 4 ~Xm
```

## Output Format

```
Good morning, aviz!

### Yesterday
- Completed: [X tasks]
- Carried over: [Y tasks]

### Today's Focus
1. [Task 1] ~Xh - [why this is priority]
2. [Task 2] ~Xh
3. [Task 3] ~Xh

Total: ~Xh of focused work

### Inbox Processed
- [N] items categorized

Ready to start?
```
