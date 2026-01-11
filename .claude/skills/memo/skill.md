# Memo Skill - Personal Memory System

Record and retrieve observations about user's work patterns, habits, and preferences.

## First: Check the Clock

Before recording or recalling, run: `date "+%Y-%m-%d %H:%M:%S %Z"`

Time context is essential for memos - patterns are time-sensitive.

## Purpose
Make Claude more personal and adapted to aviz's work style by:
- Recording patterns as they emerge
- Retrieving relevant memories when context matches
- Learning from what works and what doesn't

## Data Location
`data/memo.md` - Single searchable file with tagged entries

## Tags (for search)

### Behavior Tags
- `#timing` - Time-related patterns (late starts, extended breaks, etc.)
- `#energy` - Energy levels, drops, what helps
- `#habit` - Recurring behaviors
- `#preference` - How user likes things done
- `#blocker` - What gets in the way
- `#success` - What worked well
- `#pattern` - General patterns

### Context Tags
- `@standup` - Relevant during daily standup
- `@planning` - Relevant when planning
- `@night` - Night session specific
- `@morning` - Morning specific
- `@focus` - Deep work sessions
- `@review` - Weekly review relevant

### Project Tags
- Use project names: `@my-course` `@252events` `@dreemz` `@vocalvault` `@fabula` etc.

## When to RECORD (proactively)

Record a memo when you notice:
1. **Time pattern** - Break extended, session ran long/short, late start
2. **Energy pattern** - When energy dropped, what helped
3. **Preference expressed** - User states how they like something
4. **Success** - Something worked particularly well
5. **Blocker** - Something got in the way
6. **Habit** - Recurring behavior (positive or negative)

### Entry Format
```markdown
### YYYY-MM-DD HH:MM #tag1 #tag2 @context
**Observation:** What happened factually
**Insight:** What this means for future interactions
```

## When to RECALL (proactively)

Retrieve relevant memos during:
1. **Standup** - Search `@standup` `#timing` `#habit`
2. **Planning** - Search `@planning` `#preference` `#pattern`
3. **Energy drop** - Search `#energy` `#blocker`
4. **Similar context** - Search relevant `@context` or `@project`
5. **Weekly review** - Search `#success` `#blocker` `#pattern`

## Usage Examples

### Recording
When user extends a break:
```
I notice you extended the break. Let me note this pattern.
[Add entry to memo.md]
```

### Recalling
During standup:
```
[Search memo.md for @standup #timing]
Based on past patterns, I see you often start later than planned...
```

## Integration with GTD

- Use during `/standup` - recall timing patterns
- Use during `/boost` - recall energy strategies that worked
- Use during `/review` - surface patterns for reflection
- Use during `/prioritize` - recall preference patterns
