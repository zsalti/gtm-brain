# Memory Index

This is your persistent memory system. Each line points to a memory file that Claude will search and reference across conversations.

Format: `- [Title](filename.md) — one-line description`

**Guidelines:**
- Keep this index under 200 lines (roughly 40-50 memories max before archiving old ones)
- New memories go at the top
- Delete or archive old memories that are no longer relevant
- Update descriptions as memories evolve

## Instructions

1. As you create memories, add them here (one line per memory)
2. When you run `/mem-search`, Claude searches across all files listed here
3. Keep it tidy - this index loads into every conversation

---

Add your first memory here after running the setup skill.

