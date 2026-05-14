# Contributing to filmstack

filmstack is a collection of Markdown skill files. Contributing means writing, improving, or extending those files — no build system, no dependencies, no runtime.

## What we need

**New skills** — workflows that don't exist yet:
- `/co-production` — international co-production structure and treaty eligibility
- `/adr-session` — ADR (Automated Dialogue Replacement) preparation checklist
- `/dcp-delivery` — DCP creation and theatrical delivery checklist
- `/press-kit` — EPK (Electronic Press Kit) structure for festival submissions

**Improved existing skills** — the current skills are v1. They can be:
- More specific (more precise page count conventions, more current union rates)
- Better calibrated (does the /coverage tone feel right to working readers?)
- More accurate (union agreements change — flag outdated rates)
- More complete (are there clearance categories /rights-clearance is missing?)

**International adaptations** — filmstack is currently US-centric:
- UK: BECTU, Equity, WGGB agreements
- Canada: ACTRA, DGC, WGC agreements
- Australia: Equity Australia, AWG
- Taiwan/Asia: Local production contexts

## How to add a skill

### 1. Create the skill directory

```bash
mkdir skills/your-skill-name
```

### 2. Write the SKILL.md

Every SKILL.md follows this structure:

```markdown
---
name: your-skill-name
description: One-sentence description for auto-discovery. This is what appears
             in the skills list and helps the agent decide when to invoke this skill.
---

# /your-skill-name — Role Title

[1-2 sentences describing the character/role the AI plays]

## When to use this skill

[Specific, concrete trigger conditions — not "when you need X" but
"run this after /coverage has identified Y" or "use this before signing Z"]

## Input

[What the skill reads — files, user input, prior skill outputs]

## Process

[Numbered steps. Be specific. Include decision criteria, not just actions.]

## Output

[What the skill produces. Include the exact output format if it matters.
Include the .filmstack/ filename it saves to.]

## Tone

[If the role has a specific tone that differs from default — e.g., "clinical,
not encouraging" or "direct, not diplomatic"]

## Notes

[Edge cases, important constraints, what the skill explicitly cannot do]
```

### 3. Add to README.md

Add your skill to the pipeline table in `README.md` with stage, name, role, and description.

### 4. Add to docs/skills.md

Add a full "Skill Deep Dive" section with philosophy, industry context, and key behavior notes.

### 5. Test it

Run the skill on a real project (or a well-known film — many scripts are publicly available for educational use). Does the output look like something a professional in that role would actually produce? Show the test output in your PR.

## Quality bar

A filmstack skill is good when a working professional in that role would read the output and say "yes, that's what I would have written." Not "that's impressive for an AI" — "that's what I would have written."

The test for `/coverage` is: would a professional script reader be comfortable putting their name on this coverage? The test for `/breakdown` is: would a 1st AD trust this to build a schedule from?

If the answer is "almost but not quite," that is what the PR description should say — and it's still a contribution worth making.

## What not to contribute

- Skills that duplicate existing skills with minor variations
- Skills that require external APIs, credentials, or paid services to function
- Skills where the AI cannot reasonably produce professional-quality output (e.g., music composition, visual design decisions that require seeing the image)
- Skills for workflows where errors have irreversible real-world consequences without a strong disclaimer (financial advice, legal advice without a disclaimer equivalent to `/rights-clearance` and `/wga-check`)

## Updating union rates and industry standards

Union agreements, delivery specifications, and festival requirements change. If you spot an outdated rate or requirement:

1. Open an issue with the specific outdated information and the correct current source
2. Link to the official source (wga.org, sagaftra.org, the festival's official website)
3. PR the correction with the source in the commit message

Do not update union rates from memory. Link to the authoritative source.

## Questions

Open an issue. This project is new and the conventions are still forming.
