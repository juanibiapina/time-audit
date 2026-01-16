# Notes

A Raycast extension for interacting with Markdown notes in your Obsidian vault.

## Commands

### Track Time

Log timestamped entries to track what you worked on.

1. Trigger "Track Time" command in Raycast
2. Type what you worked on
3. Press Enter to log the entry

Entries are logged in the format `- HH:mm: Your entry` under a `## Tracking` section.

### Log

Add simple entries without timestamps.

1. Trigger "Log" command in Raycast
2. Type your entry
3. Press Enter to log the entry

Entries are logged in the format `- Your entry` under a `## Log` section.

## Configuration

| Preference          | Description                 |
| ------------------- | --------------------------- |
| Obsidian Vault Path | Path to your Obsidian vault |

## Daily Note Format

Both commands write to `daily/YYYY-MM-DD.md` in your vault.

If the file doesn't exist, it creates:

```markdown
---
tags:
  - daily
---

# YYYY-MM-DD

## Section

- Your entry
```

If the file exists but has no matching section, the section is appended. If the section exists, entries are added at the end of it.
