# Claude Tasks

A GTD-based personal task management system powered by Claude Code.

## Quick Start

```bash
cd /Users/aviz/tasks
claude
```

Then run `/standup` to start your day!

## Commands

| Command | Description |
|---------|-------------|
| `/add <task>` | Quick add task to inbox |
| `/today` | Show today's tasks |
| `/done <task>` | Mark task complete |
| `/standup` | Daily planning |
| `/review` | Weekly review |
| `/prioritize` | Re-prioritize all tasks |
| `/week` | Week overview |
| `/focus [time]` | Enter focus mode |
| `/inbox` | Process inbox items |
| `/project <name>` | Create/switch project |

## Task Format

```
- [ ] Task description @project #tag !priority ~estimate
```

- **Priority:** `!high`, `!medium`, `!low`
- **Estimate:** `~15m`, `~30m`, `~1h`, `~2h`, `~4h`
- **Project:** `@project-name`
- **Tags:** `#code`, `#docs`, `#meeting`, etc.

## Daily Workflow

1. **Morning:** `/standup` - Plan your day
2. **During day:** `/add` tasks as they come
3. **Working:** `/focus 25m` for pomodoro sessions
4. **Complete:** `/done task-name` when finished

## Weekly Workflow

1. **Friday:** `/review` - Retrospective
2. Process backlog
3. Plan next week

## File Structure

```
tasks/
├── inbox.md      # Capture everything here
├── today.md      # Today's focus (max 3)
├── backlog.md    # Prioritized by Eisenhower matrix
├── someday.md    # Future ideas
└── archive/      # Completed tasks by date
```

## Skills (Auto-Applied)

- **task-parsing** - Converts natural language to structured tasks
- **priority-matrix** - Eisenhower matrix prioritization
- **time-estimation** - Estimates task duration

## Sub-Agents

- **task-planner** - Breaks down complex tasks
- **task-reviewer** - Reviews and cleans up tasks
- **daily-standup** - Morning planning
- **retrospective** - Weekly reflection

## Privacy

Your actual tasks are gitignored. Only the system structure and example files are committed.

---

Built with Claude Code sub-agents, skills, and slash commands.
