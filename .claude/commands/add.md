---
description: Quick add a task to inbox
argument-hint: <task description>
allowed-tools: Read, Edit
---

# Add Task to Inbox

Add the following task to the inbox: $ARGUMENTS

## Instructions

1. Read the current inbox at `tasks/inbox.md`
2. Parse the task using the task-parsing skill:
   - Extract priority (!high, !medium, !low)
   - Estimate time (~15m, ~30m, ~1h, ~2h, ~4h)
   - Detect project (@project-name)
   - Add relevant tags (#tag)
3. Format as: `- [ ] Task description @project #tag !priority ~estimate`
4. Add the new task under "## Unprocessed Tasks" in inbox.md
5. Confirm what was added

## Example

Input: `/add Review PR #123 urgently`
Output: Added to inbox: `- [ ] Review PR #123 @work #review !high ~30m`
