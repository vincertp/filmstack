# Architecture

## Design principles

filmstack follows the same core pattern as gstack: **role-based AI agents with explicit input/output contracts, connected by a shared file state**.

### 1. Skills are stateless

Each skill reads from `.filmstack/` context files and writes to `.filmstack/` context files. Skills do not share memory between invocations. This means:
- Any skill can be run independently without running prior skills first
- Any skill can be run multiple times (on different drafts, at different stages)
- The skill chain is composable — you can skip skills, reorder them, or loop

### 2. The `.filmstack/` directory is the state machine

Every skill that produces persistent output writes to `.filmstack/`. Every skill that consumes prior output reads from `.filmstack/`. The directory accumulates project knowledge over time.

```
.filmstack/
├── creative-brief.md        ← /pitch-room output
├── coverage-2026-01-15.md   ← /coverage output (versioned by date)
├── script-doctor-2026-01-20.md
├── market-comp-2026-01-22.md
├── breakdown-2026-02-01.md
├── casting-breakdown-2026-02-01.md
├── budget-review-2026-02-03.md
├── picture-lock-2026-04-15.md
├── rights-clearance-2026-04-20.md
├── wga-check-2026-01-10.md
├── festival-strategy-2026-04-25.md
└── retro-production-2026-03-30.md
```

### 3. Skills are self-describing

Each `SKILL.md` file is simultaneously:
- The prompt that instructs the AI how to behave
- Human-readable documentation of what the skill does
- A machine-readable manifest (YAML frontmatter) for auto-discovery

No separate registry. No configuration files. The skill IS the documentation.

### 4. Roles create cognitive load reduction

The most important design decision in filmstack is the role assignment. When you run `/coverage`, the AI is not "Claude being asked to do coverage" — it is a specific character (a professional script reader) with a specific identity, specific constraints, and specific output format. This matters because:

- Role clarity reduces hallucination. A script reader who knows they cannot recommend every script resists the urge to be encouraging.
- Role constraints create consistent output format. Buyers and collaborators know what to expect from a filmstack coverage report.
- Role identity creates appropriate tone. A line producer's tone is different from a story editor's, which is different from a rights consultant's.

### 5. Warnings are explicit and non-negotiable

Every skill that touches legal, financial, or compliance territory carries an explicit disclaimer. These disclaimers are:
- Non-removable (they are part of the skill definition)
- Specific (they name what this skill cannot substitute for)
- Actionable (they say what to do instead)

This is not liability protection theater. It is an honest communication of what AI analysis can and cannot do.

## Pipeline data flow

```
/pitch-room
    ↓ creative-brief.md
/coverage ←── script file
    ↓ coverage-[date].md
/script-doctor ←── coverage-[date].md
    ↓ script-doctor-[date].md
/market-comp ←── creative-brief.md, coverage
    ↓ market-comp-[date].md
        ↓
/breakdown ←── production draft script
    ↓ breakdown-[date].md
/casting-breakdown ←── script
    ↓ casting-breakdown-[date].md
/budget-review ←── breakdown-[date].md, market-comp-[date].md
    ↓ budget-review-[date].md
        ↓
[PRODUCTION]
        ↓
/picture-lock
    ↓ picture-lock-[date].md
/rights-clearance
    ↓ rights-clearance-[date].md
/wga-check
    ↓ wga-check-[date].md
        ↓
/festival-strategy ←── market-comp, picture-lock
    ↓ festival-strategy-[date].md
        ↓
/retro ←── all .filmstack/ files
    ↓ retro-[phase]-[date].md
```

## How to add a skill

1. Create a directory under `skills/` with the skill name
2. Create `SKILL.md` inside it with YAML frontmatter:
   ```yaml
   ---
   name: skill-name
   description: One-sentence description for auto-discovery
   ---
   ```
3. Define: Role, When to use, Input, Process, Output format
4. Add to the `CLAUDE.md` skills list in the install instructions
5. Update `docs/skills.md` with a full description

## Why not a Python/Node app?

Markdown skills that run inside Claude Code have no dependencies, no runtime environment, no build step, and no maintenance surface. They work across any agent that supports the SKILL.md standard. They are readable, forkable, and modifiable by anyone who can edit text.

The tradeoff: no programmatic validation, no automated testing, no deterministic output. These are judgment-intensive workflows — the AI judgment is the feature, not a limitation to work around.
