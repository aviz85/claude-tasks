---
description: Enter focus mode - single task deep work
argument-hint: [duration like 1h, 2h, or 25m for pomodoro]
allowed-tools: Read
---

# Focus Mode

Starting focus session: $ARGUMENTS

## Context
- Today's focus tasks: !`grep -A 10 "## Focus" tasks/today.md 2>/dev/null | head -5`

## Instructions

1. **Identify focus task**:
   - Take the first incomplete task from today's Focus section
   - Or user can specify which task

2. **Set up focus session**:
   - Duration: $ARGUMENTS (default: 25m pomodoro)
   - Single task only
   - No context switching

3. **Display focus view**:
   - Show ONLY the current task
   - Hide all other tasks
   - Show timer countdown

4. **Focus rules**:
   - If new task comes up → capture to inbox, return to focus
   - If blocked → note blocker, switch to next focus task
   - If complete early → take a break or start next

## Output Format

```
## Focus Mode Active

### Current Task
[The one task you're working on]

### Duration
[X] minutes remaining

### Rules
- New ideas → /add to inbox
- If blocked → note it, move on
- When done → /done [task]

### Blockers Noted
(none yet)

---
Focus. You've got this.
```

## End Focus

When time is up or task is done:
- Log time spent
- Mark task complete if finished
- Suggest short break (5 min after 25m, 15 min after 90m)
