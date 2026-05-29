# Installation Guide

Choose your path based on your comfort level with GitHub.

## Path 1: Fastest (Recommended) - Use the Setup Skill

**Best for:** Anyone, takes 30 minutes total

```
Open Claude Code or Claude Coworker
Run: /setup-memory-system https://github.com/zsalti/gtm-brain
```

The skill will:
1. Ask 5 simple questions about your role, tone, and patterns
2. Create your `.claude/` folder structure
3. Generate your personalized `brand-voice.md` and `strategy-guard.md`
4. Create your first memory
5. Show you a checklist - you're done

No manual file editing. No GitHub knowledge needed.

---

## Path 2: Fork on GitHub (If You Want Version Control)

**Best for:** Teams, or if you want to version control your memory system

1. Go to https://github.com/zsalti/gtm-brain
2. Click **Fork** (top right)
3. In your fork, clone it locally:
   ```
   git clone https://github.com/YOUR-USERNAME/gtm-brain.git
   ```
4. Copy the `memory/`, `.claude/rules/`, and `.claude/commands/` folders into your project
5. Read ONBOARDING.md for customization steps
6. Commit and push your customizations back to your fork

This keeps your memory system in version control alongside your project.

---

## Path 3: Manual (Full Control)

**Best for:** Advanced users, or if you want to pick and choose which files to include

1. Create these folders in your project:
   ```
   .claude/rules/
   .claude/commands/
   memory/
   ```

2. Copy files from https://github.com/zsalti/gtm-brain:
   - `memory/MEMORY.md`
   - `memory/_template_*.md` (all four templates)
   - `.claude/rules/learning-loop.md`
   - `.claude/rules/_template-brand-voice.md` and `_template-strategy-guard.md`
   - `.claude/commands/setup-memory-system.md` (if you want the interactive setup)

3. Customize as needed (see ONBOARDING.md)

---

## After Installation

Whichever path you choose:

1. Make sure Claude Code recognizes your `.claude/` folder (it auto-loads rules)
2. In your next Claude session, run `/mem-search "test"` to verify memory works
3. You're live - start using it immediately

If anything breaks, check ONBOARDING.md troubleshooting section.
