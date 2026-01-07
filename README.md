# Claude Tasks

A GTD-based personal task management system powered by Claude Code.

## Installation

```bash
# Clone the repository
git clone https://github.com/aviz85/claude-tasks.git
cd claude-tasks

# Create your personal task files (gitignored)
cp tasks/inbox.example.md tasks/inbox.md
cp tasks/today.example.md tasks/today.md
cp tasks/backlog.example.md tasks/backlog.md
cp tasks/someday.example.md tasks/someday.md

# Start Claude Code
claude
```

Then run `/standup` to start your day!

## iPhone App (PWA)

Use Claude Tasks on your iPhone as a Progressive Web App:

### Installation

1. **Deploy to GitHub Pages:**
   ```bash
   # Enable GitHub Pages for the 'docs' folder in your repo settings
   # Your app will be available at: https://your-username.github.io/claude-tasks/app.html
   ```

2. **Install on iPhone:**
   - Open Safari on your iPhone
   - Navigate to `https://your-username.github.io/claude-tasks/app.html`
   - Tap the Share button (square with arrow)
   - Scroll down and tap "Add to Home Screen"
   - Tap "Add" in the top right

3. **Launch the app:**
   - Find the "Tasks" icon on your home screen
   - Tap to open - it works like a native app!

### Features

- ✓ Works offline (once loaded)
- ✓ Full GTD task management
- ✓ Inbox, Today, and All Tasks views
- ✓ Swipe left to delete tasks
- ✓ Priority levels (!high, !medium, !low)
- ✓ Time estimates (~15m, ~30m, ~1h, etc.)
- ✓ Projects and tags
- ✓ Data stored locally on your device

### Quick Start (iPhone)

1. Tap the `+` button to add a task
2. Set priority and time estimate
3. Add to Today for focus tasks (max 3 recommended)
4. Tap checkbox to complete tasks
5. Swipe left to delete tasks

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
