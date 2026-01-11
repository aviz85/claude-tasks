---
description: Show week overview and upcoming tasks
allowed-tools: Read, Glob
---

# Week Overview

## First: Check the Clock
Current time: !`date "+%Y-%m-%d %H:%M:%S %Z"`

## Context
- Today: !`date +%Y-%m-%d`
- Day of week: !`date +%A`
- Today's tasks: !`cat tasks/today.md 2>/dev/null`
- Backlog: !`cat tasks/backlog.md 2>/dev/null`
- Recent completions: !`ls -la tasks/archive/ 2>/dev/null | tail -7`

## Instructions

1. Show current week status:
   - What day is it?
   - Days remaining in the week
   - Tasks completed this week (from archive)

2. Summarize what's planned:
   - Today's focus tasks
   - High priority items in backlog
   - Upcoming deadlines

3. Show weekly capacity:
   - Estimated hours of work in backlog
   - Realistic capacity remaining

## Output Format

```
## Week of [DATE]

### This Week's Progress
- Monday: [X tasks completed]
- Tuesday: [X tasks completed]
- ...
- Today ([DAY]): [X tasks planned]

### Remaining This Week
- High Priority: [N tasks, ~Xh]
- Medium Priority: [N tasks, ~Xh]

### Upcoming Deadlines
- [Task] - Due [DATE]

### Capacity Check
- Remaining days: [N]
- Planned work: ~[X]h
- Status: [On track / At risk / Overloaded]
```
