# Onboarding Guide (5 Steps, ~30 Minutes)

After running `/setup-memory-system`, use this guide to understand and customize your system.

## Step 1: Understand the Architecture (5 min)

**What you have:**
- `.claude/rules/` folder - contains 3 files that auto-load and shape Claude's behavior
- `memory/` folder - stores all your learnings (searchable with `/mem-search`)
- `setup-memory-system.md` - the skill that scaffolds everything

**How it works:**
1. When you open Claude Code, it auto-loads files in `.claude/rules/`
2. Your brand voice rule tells Claude your tone, patterns, and forbidden terms
3. Your strategy guard rule prevents off-strategy work by catching known patterns
4. Your learning loop rule enforces: before strategy work (check memory), after work (log findings)
5. Any memory file in `memory/` is searchable via `/mem-search`

**Key insight:** This isn't a chatbot. These are rules that load into the context, shaping how Claude thinks about your work.

---

## Step 2: Customize Brand Voice (5-7 min)

Open `.claude/rules/brand-voice.md` and fill in these sections:

**[YOUR PERSONA]**
- Example: "Kickass B2B marketer with no-nonsense, helpful content"
- Your version: [What's your role? What's your vibe?]

**[YOUR PRIMARY TONE]**
- Example: "Authoritative but conversational - like an experienced peer walking you through something"
- Your version: [How should Claude write for/as you?]

**[YOUR CORE PRINCIPLE]**
- Example: "Walking with the reader - thinking alongside, not standing above"
- Your version: [What's the single most important thing about your voice?]

**Language rules**
- Add your terms (jargon native to your industry)
- Add your forbidden terms (words you hate)

**Signature patterns**
- List 2-3 openings you actually use
- List 2-3 transitions you actually use
- List 2-3 reframes you actually use

(The template has examples - edit them to match your actual patterns, not made-up ones.)

**Why this matters:** After this step, Claude uses YOUR voice, not generic consulting-speak.

---

## Step 3: Fill in Your Roadmap (5 min)

Open `roadmap.md` and answer these four prompts:

**90-Day Goals**
- Example: "Hit $10K/month ARR and convert 2 pilots to retainers"
- Your version: [What do you want to achieve in 90 days?]

**Three Main Objectives (North Stars)**
- Example: "Close existing pipeline, Fill funnel with leads, Build thought leadership"
- Your version: [What are your 3 strategic pillars?]

**What You Want to Improve**
- Example: "Sales follow-up velocity, Content differentiation, Lead qualification"
- Your version: [What's broken that you want to fix?]

**Two or Three Main Targets (What "Done" Looks Like)**
- Example: "2 retainers signed ($10K/mo), 50 qualified inbound leads, 2K newsletter subscribers"
- Your version: [What are your 2-3 measurable outcomes?]

**Why this matters:** This roadmap becomes your decision filter. Every time you're tempted to start something new, Claude will ask: "Does this serve one of your three objectives or targets?" If not, it's a distraction.

---

## Step 4: Customize Strategy Guard (5-7 min)

Open `.claude/rules/strategy-guard.md` and fill in these sections:

**[YOUR PROFILE/WIRING]**
- Example: "4-3-9-3 Kolbe (Quick Start 9), Type 3 Enneagram (achievement-driven)"
- Your version: [What's your personality type? Your key pattern?]

**[YOUR PATTERN]**
- Example: "Exciting new idea → abandons current plan → builds something complex → doesn't finish"
- Your version: [What's the cycle you get stuck in?]

**[YOUR CURE]**
- Example: "The roadmap is the cure" or "Finish before starting"
- Your version: [What breaks your pattern?]

**Red flag patterns**
- Keep "Shiny Object" pattern (everyone has this)
- Edit the others to match YOUR known distractions

**Decision framework**
- Keep the 6 questions (these are universal)
- Customize the examples

**Why this matters:** This rule will catch you trying to abandon the plan mid-sprint and say "wait, that's your Quick Start 9 talking."

---

## Step 5: Create Your First Memory (5-10 min)

The setup skill walked you through this, but here's the structure:

**Memory file naming:**
- `memory/user_role.md` - who you are
- `memory/feedback_learning.md` - a lesson learned
- `memory/project_initiative.md` - current work
- `memory/reference_tool.md` - pointer to external system

**YAML frontmatter** (copy this structure):
```
---
name: My First Memory
description: One-line hook for future recall
type: user (or feedback, project, reference)
---

Content goes here.
```

**Then update `memory/MEMORY.md`** with a pointer:
```
- [My First Memory](user_role.md) - One-line description
```

**Example memory:**
```yaml
---
name: User Role
description: Data scientist investigating logging infrastructure
type: user
---

I'm a data scientist on a 4-person team focused on observability. I have strong Python/ML background but this is my first time in the React side of this codebase. Frame frontend explanations in terms of backend analogues (data pipelines, transformations, etc.) where possible.
```

**Why this matters:** This is the seed. Once you create one memory, the pattern is clear and `/mem-search` starts working.

---

## Step 5: Test Memory Search (2 min)

In your next Claude session, run:
```
/mem-search "first memory topic"
```

Claude will search your `memory/` folder and return matching findings.

If nothing comes back, check:
1. Did you save `memory/MEMORY.md` with an entry pointing to your memory file?
2. Is the memory file in the right folder (`memory/`)?
3. Run `/mem-search` again - sometimes it takes a moment to index.

**Why this matters:** This proves the system is live. Everything from here on is just using it.

---

## Troubleshooting

**Q: The setup skill didn't run**
A: Make sure you're in Claude Code or Claude Coworker, not the web UI. Rules and skills require the full app.

**Q: `/mem-search` returns nothing**
A: Check that your memory file is in the `memory/` folder and `MEMORY.md` has an entry for it.

**Q: I edited brand-voice.md but Claude didn't change tone**
A: Close and reopen Claude Code. Rules are loaded on startup.

**Q: Can I edit these rules later?**
A: Yes. The templates are just starting points. Edit them anytime.

**Q: Do I have to fill in every section of brand-voice?**
A: No. Fill in what's relevant. If your writing doesn't have signature patterns, leave that section minimal. Honest is better than comprehensive.

---

## Next Steps

1. ✅ Setup complete
2. ✅ Brand voice customized
3. ✅ Strategy guard customized
4. ✅ First memory created
5. ✅ `/mem-search` tested

Now:
- Start using Claude Code as usual
- Create memories as you learn things (use `/mem-search` to check if you already covered a topic before doing research)
- Update brand-voice and strategy-guard rules as you discover new patterns
- Your rules auto-load each session

That's it. The system works forever from here.

---

## Reading List (Optional)

- README.md - overview of the whole system
- SETUP.md - if you want different installation options
- `.claude/rules/learning-loop.md` - the third rule you have (before/after workflow)
- `.claude/rules/_template-rule.md` - if you want to create custom rules beyond brand-voice and strategy-guard

You don't need to read these. The system works without them. But they're there if you're curious.
