# /memo - Quick Memory Capture

Intelligently capture a memo about what just happened.

## Behavior

**With parameters:** `/memo <text>` - Record the given text as memo
**Without parameters:** `/memo` - Analyze recent context and guess what to memo

## When Called Without Parameters

Analyze the conversation to identify what just happened that's worth remembering:

1. **Success pattern** - User achieved something, workflow worked well
2. **Energy observation** - User mentioned tiredness, motivation, or energy state
3. **Preference revealed** - User expressed how they like things done
4. **Blocker identified** - Something that blocked progress
5. **Timing insight** - Best time for certain activities discovered
6. **Habit pattern** - Recurring behavior noticed

## Instructions

1. Look at the last 3-5 exchanges in conversation
2. Identify the most notable/memorable thing that happened
3. Guess why user triggered /memo (what caught their attention?)
4. Use the memo skill to record it

## Output Format

```
📝 Detected: [what you noticed]
Recording: [the memo entry]

✓ Saved to data/memo.md
```

## Examples

**After user says "wow that worked perfectly":**
```
📝 Detected: Success with [feature/workflow]
Recording: [timestamp] #success @[context] - [what worked and why]
```

**After user mentions being tired:**
```
📝 Detected: Energy state observation
Recording: [timestamp] #energy @night - User energy dropping at [time], consider break
```

**After user expresses preference:**
```
📝 Detected: Preference revealed
Recording: [timestamp] #preference - User prefers [X] over [Y] because [reason]
```

## Skill Reference

Use the memo skill format:
```markdown
### YYYY-MM-DD HH:MM #tag1 #tag2 @context
**Observation:** What happened
**Insight:** Why it matters / pattern identified
```

Tags: #timing #energy #habit #preference #blocker #success #pattern
Contexts: @standup @planning @night @morning @focus @review @development
