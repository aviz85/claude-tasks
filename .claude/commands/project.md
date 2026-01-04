---
description: Create or switch to a project
argument-hint: <project-name>
allowed-tools: Read, Write, Edit, Bash, Glob
---

# Project Management

Project: $ARGUMENTS

## Context
- Existing projects: !`ls -d projects/*/ 2>/dev/null || echo "No projects yet"`
- Project folder: !`ls projects/$ARGUMENTS/ 2>/dev/null || echo "Project doesn't exist"`

## Instructions

### If project doesn't exist → Create it

1. Create folder: `projects/$ARGUMENTS/`
2. Create README.md:
   ```markdown
   # Project: [NAME]

   ## Overview
   [Brief description]

   ## Goals
   - [ ] Goal 1
   - [ ] Goal 2

   ## Status
   - Created: [DATE]
   - Status: Active
   ```
3. Create tasks.md:
   ```markdown
   # [PROJECT] Tasks

   ## In Progress

   ## Todo

   ## Done
   ```
4. Confirm creation

### If project exists → Show status

1. Read project README and tasks
2. Show:
   - Project overview
   - Current tasks in progress
   - Pending tasks count
   - Completed tasks count

## Output Format

### New Project
```
## Created Project: [NAME]

Files created:
- projects/[name]/README.md
- projects/[name]/tasks.md

Next: Add tasks with /add [task] @[project]
```

### Existing Project
```
## Project: [NAME]

### Overview
[From README]

### Progress
- In Progress: [N] tasks
- Todo: [N] tasks
- Completed: [N] tasks

### Current Focus
- [Task 1]
- [Task 2]

Use /add [task] @[project] to add tasks
```
