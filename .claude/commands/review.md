---
description: Weekly review - retrospective and planning
allowed-tools: Read, Edit, Glob
skills: priority-matrix, time-estimation
---

# Weekly Review

## First: Check the Clock
Current time: !`date "+%Y-%m-%d %H:%M:%S %Z"`

## Context
- Today: !`date +%Y-%m-%d`
- This week's archive: !`ls tasks/archive/ 2>/dev/null | tail -7`
- Current backlog: !`cat tasks/backlog.md 2>/dev/null`
- Someday list: !`cat tasks/someday.md 2>/dev/null`
- Inbox: !`cat tasks/inbox.md 2>/dev/null`

## Weekly Review Checklist

### 1. Clear Inbox (Zero Inbox)
- Process ALL remaining inbox items
- Nothing should stay in inbox over weekend

### 2. Review Completed Work
- Read through this week's archive
- Count total tasks completed
- Identify wins and accomplishments

### 3. Review Incomplete Work
- What didn't get done?
- Why? (blockers, priority change, too ambitious)
- Should it stay on backlog or be removed?

### 4. Review Someday/Maybe
- Any items ready to become active?
- Any items to delete (no longer relevant)?

### 5. Process Projects
- Check each project folder
- Are projects on track?
- Any stale projects to archive?

### 6. Plan Next Week
- Top 3 priorities for next week
- Any deadlines coming up?
- Realistic capacity check

## Output Format

```
## Weekly Review - Week of [DATE]

### Accomplishments
- Completed [N] tasks this week
- Key wins:
  - [Win 1]
  - [Win 2]

### What Didn't Happen
- [Task] - [reason]
- [Task] - moving to next week

### Stale Items (> 7 days untouched)
- [Task] - Recommend: [keep/archive/delete]

### Next Week's Focus
1. [Priority 1]
2. [Priority 2]
3. [Priority 3]

### Process Improvements
- [What went well]
- [What to improve]

Ready for next week!
```
