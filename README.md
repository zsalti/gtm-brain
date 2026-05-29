# GTM Brain - Persistent Memory System for Claude Code & Claude Coworker

A complete memory system that persists across conversations in Claude Code and Claude Coworker. Never repeat yourself. Keep learnings from every session. Shape Claude's behavior with custom behavioral rules.

## What This Is

GTM Brain is a **memory architecture + behavioral rules framework** for Claude Code. Instead of manually updating skills or context files each time, this system:

- **Persists learnings** across conversations (user profile, project context, strategic decisions, external resource links)
- **Auto-loads behavioral rules** that shape how Claude approaches your work (brand voice, strategy guard, learning loop)
- **Provides searchable memory** so Claude can recall prior decisions, market findings, and lessons learned
- **Guides Claude's behavior** with rules that prevent you from having to repeat the same guidance twice

## Why It's Good

1. **Claude remembers who you are** - Your role, expertise, preferences, and working style load automatically
2. **Strategic consistency** - Custom rules (brand voice, strategy guard) enforce your thinking patterns and guardrails
3. **No repeat guidance** - Instead of "use this tone" every time, your brand voice loads automatically
4. **Searchable history** - "Did we research X before?" → `/mem-search` finds it in seconds
5. **Cross-session context** - Learnings from May 15 are available in June's conversations
6. **Works offline** - Everything lives in your local `.claude/` folder (no external databases)

## Why It's Better Than Individual Skills

**Individual skills approach:**
- Update a skill each time you learn something new
- Manually paste context into each Claude session
- No way to search prior decisions or findings
- Brand voice rules live in your head, not in code
- "Did we solve this before?" → manual digging through old chat history

**GTM Brain approach:**
- One `/mem-search` finds learnings from any prior session
- Auto-load your brand voice, strategic rules, and project context in 30 seconds
- Custom rules prevent off-strategy work before it starts
- Learning loop enforces consistent documentation after each session
- Setup takes 30 minutes, then it works forever

## How to Install

### Fastest Way (Recommended)

1. **Open Claude Code or Claude Coworker**
2. **Run this command:**
   ```
   /setup-memory-system https://github.com/zsalti/gtm-brain
   ```
3. **Answer 5 questions** (20-30 minutes, conversational)
4. **Done.** Your memory system is live.

### Manual Way (Full Control)

1. Clone or fork https://github.com/zsalti/gtm-brain
2. Copy the `memory/`, `.claude/rules/`, and `.claude/commands/` folders into your project
3. Read `ONBOARDING.md` for next steps

## File Structure

```
your-project/
├── roadmap.md                        # your 90-day goals, objectives, targets
├── .claude/
│   ├── rules/
│   │   ├── learning-loop.md          # (auto-loaded) enforces before/after workflow
│   │   ├── brand-voice.md            # (auto-loaded) your tone, patterns, forbidden terms
│   │   └── strategy-guard.md         # (auto-loaded) prevents off-strategy work + roadmap alignment
│   └── commands/
│       └── setup-memory-system.md    # skill that scaffolds everything
├── memory/
│   ├── MEMORY.md                     # index of all memories (auto-loaded, ~200 lines)
│   ├── user_*.md                     # who you are, expertise, preferences
│   ├── feedback_*.md                 # lessons learned, guidance, patterns
│   ├── project_*.md                  # current initiatives, deadlines, context
│   └── reference_*.md                # pointers to external systems (Linear, Slack, etc.)
└── ...rest of your project
```

## Your Roadmap

GTM Brain includes a `roadmap.md` file that anchors all strategic decisions. Fill it in once with:

- **90-day goals** - What you want to achieve in the next quarter
- **Three main objectives** - Your north stars (the 3 things that matter most)
- **What you want to improve** - Areas that are weak and need fixing
- **Two or three main targets** - Measurable outcomes that prove progress

Whenever you're brainstorming or making strategic decisions, Claude automatically checks:
- "Does this serve one of your three objectives?"
- "Does this move the needle on one of your targets?"
- "Or is this a distraction?"

This is your decision filter. It prevents off-strategy work before it starts.

## Memory Types

- **user:** Your role, expertise, knowledge, preferences, working style
- **feedback:** Lessons learned, guidance you've received, patterns you've confirmed
- **project:** Current initiatives, deadlines, constraints, strategic context
- **reference:** Pointers to external systems (where to find X, when to check Y)

## Behavioral Rules (Auto-Loaded)

- **learning-loop.md:** Before strategy work: check memory + scan strategy docs. After work: log findings + update hypotheses.
- **brand-voice.md:** Tone, voice patterns, forbidden terms, writing mechanics (customizable to your persona)
- **strategy-guard.md:** Prevents off-strategy work by pattern-matching against your known distractions (customizable)

## Quick Start

1. Run `/setup-memory-system`
2. Answer 5 conversational questions
3. Read `ONBOARDING.md` if you want deeper context
4. In your next Claude session, try `/mem-search "topic"` to find prior learnings

## Questions?

- **How does `/mem-search` work?** See ONBOARDING.md, Step 5
- **Can I customize brand voice?** Yes, see ONBOARDING.md, Step 4
- **Do I have to read all the templates?** No. The setup skill walks you through it conversationally.
- **Does this work in Claude Coworker?** Yes, same system works everywhere.

---

**Set up in 30 minutes. Save hours of repetition forever.**
