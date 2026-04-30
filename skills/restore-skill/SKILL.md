---
name: restore-skill
description: Restore archived skills from ~/.claude/skills-archive/ back into active use.
user-invocable: true
---

# restore-skill

Restore archived skills from ~/.claude/skills-archive/ back into active use.

## When to Use

- Need a skill you archived in a previous session
- Want to browse available archived skills
- Need temporary access to a skill for this session only

## How It Works

This skill orchestrates the underlying shell script to:
1. Search archived skills by keyword
2. Show you matching skills
3. Restore your selection (temp or permanent)
4. Confirm restoration

---

## Interactive Restore Flow

Ask the user for a keyword to search archived skills (or say "all" to list everything):

```bash
bash ~/.claude/restore-skill.sh --search {keyword}
```

Display the numbered list of matching skills. Then ask:

- "Which skill(s) do you want to restore? (enter skill name(s), space-separated)"

Once you have the selection, ask:

- "Restore as temporary (auto re-archive on session exit) or permanent?"

Execute the restore with user's choice:

```bash
bash ~/.claude/restore-skill.sh --restore {skill1} {skill2} ... --temp
# or
bash ~/.claude/restore-skill.sh --restore {skill1} {skill2} ... --perm
```

Show the output and confirm: "Your selected skills are now active in this session."

---

## Terminal Usage (without this skill)

```bash
# Search for skills
bash ~/.claude/restore-skill.sh --search firebase

# Restore specific skills (temp)
bash ~/.claude/restore-skill.sh --restore firebase --temp

# Restore specific skills (permanent)
bash ~/.claude/restore-skill.sh --restore firebase --perm

# Interactive mode
bash ~/.claude/restore-skill.sh

# Clean up temp restorations
bash ~/.claude/restore-skill.sh --cleanup
```

---

## Notes

- **Temporary restore**: Skill auto re-archives when you exit Claude. Useful for one-off uses.
- **Permanent restore**: Skill stays active until you manually archive it.
- **Search**: Case-insensitive keyword matching. Try partial names (e.g., "fire" finds "firebase", "firestore", etc).
- **Multiple skills**: You can restore multiple skills at once.
