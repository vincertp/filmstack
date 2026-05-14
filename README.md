# filmstack

[繁體中文](README.zh-TW.md) | English

> "Development is the process of turning money into scripts, and production is the process of turning scripts into movies."
> — William Goldman

**filmstack** is an open-source AI workflow system for film and TV development — built on the same philosophy as [gstack](https://github.com/garrytan/gstack), adapted for the entertainment industry.

It turns Claude Code (or any agent supporting the SKILL.md standard) into a virtual production team: a story editor who finds your plot holes, a line producer who pressure-tests your schedule, a script reader who gives you real Hollywood coverage, a rights clearance officer who scans for legal exposure, and a festival strategist who routes your finished film to the right markets.

**23 skills. 7 production stages. Full pipeline from logline to distribution.**

---

## The pipeline

filmstack follows the actual 7-stage Hollywood production workflow:

```
Development → Pre-Production → Production → Post-Production → Marketing → Distribution → Exhibition
```

Each skill feeds into the next. `/pitch-room` writes a creative brief that `/coverage` reads. `/breakdown` produces a scene list that `/budget-review` uses. `/picture-lock` generates a delivery checklist that `/rights-clearance` verifies.

| Stage | Skill | Role | What it does |
|---|---|---|---|
| **Development** | `/logline` | Story Consultant | Logline workshop — iterative refinement toward a single sentence that sells the film |
| **Development** | `/pitch-room` | Story Executive | Six forcing questions that challenge your concept before you write a word |
| **Development** | `/series-bible` | TV Writer / Showrunner | TV series bible structure — premise, characters, season arc, episode concepts, ongoing potential |
| **Development** | `/coverage` | Script Reader | Hollywood-standard coverage: Logline, Synopsis, Comments, Pass/Consider/Recommend |
| **Development** | `/script-doctor` | Story Editor | Find plot holes, broken character arcs, pacing problems, and unmotivated choices |
| **Development** | `/market-comp` | Development Executive | Comparable titles analysis — "A meets B" framing, box office comps, streaming benchmarks |
| **Development** | `/pitch-deck` | Packaging Specialist | Investor and distributor pitch deck — 9-slide structure with seven-test review |
| **Pre-Production** | `/breakdown` | 1st AD | Scene-by-scene breakdown: locations, cast, extras, props, VFX, special requirements |
| **Pre-Production** | `/casting-breakdown` | Casting Director | Character breakdowns in Breakdown Express format, ready for submission |
| **Pre-Production** | `/budget-review` | Line Producer | Budget feasibility, schedule risk, cost-per-day estimate, red flags |
| **Pre-Production** | `/co-production` | Co-Production Consultant | International treaty eligibility, points test, financial split, territory benefits |
| **Pre-Production** | `/wga-check` | Labor Consultant | WGA/SAG-AFTRA compliance scan — minimums, residuals, credit arbitration triggers |
| **Pre-Production** | `/rights-clearance` | Entertainment Lawyer | E&O insurance pre-check — music, clearances, life rights, trademark exposure |
| **Pre-Production** | `/taiwan-production` | Taiwan Production Consultant | 文化部輔導金, TAICCA, 金馬影展 strategy, OTT landscape, co-production eligibility |
| **Post-Production** | `/adr-session` | Post Sound Supervisor | ADR session prep — cue sheet, actor scheduling, studio checklist, KDM-free |
| **Post-Production** | `/picture-lock` | Post Supervisor | Picture lock checklist — delivery specs, VFX pulls, sound spotting, M&E requirements |
| **Post-Production** | `/dcp-delivery` | Digital Cinema Specialist | DCP creation, encryption, KDM management, theatrical delivery checklist |
| **Distribution** | `/music-licensing` | Music Supervisor | Two-license rule, sync vs. master clearance, PRO registration, cue sheet requirements |
| **Distribution** | `/distribution-deal` | Sales Agent / Entertainment Lawyer | Distribution term sheet review — MG, P&A commitment, holdback windows, net profits |
| **Distribution** | `/festival-strategy` | Sales Agent | Festival routing strategy based on content type, budget, and target (awards vs. distribution) |
| **Distribution** | `/press-kit` | Unit Publicist | EPK structure — synopsis, director statement, production notes, asset list |
| **Distribution** | `/korea-production` | Korea Production Consultant | KOFIC funding, BIFF strategy, Korean OTT landscape, Korea-Taiwan co-production framework |
| **Power Tools** | `/retro` | Producer | Production retrospective — budget variance, schedule drift, what to do differently |

---

## Quick start

1. Install filmstack (see below)
2. Run `/pitch-room` — describe what you're developing
3. Run `/coverage` on your script draft
4. Run `/script-doctor` to find structural problems
5. Stop there. You'll know if this is for you.

## Install — 30 seconds

**Requirements:** [Claude Code](https://docs.anthropic.com/en/docs/claude-code), [Git](https://git-scm.com/)

### Global install (for all your projects)

Open Claude Code and paste:

> Install filmstack: run `git clone https://github.com/YOUR_USERNAME/filmstack.git ~/.claude/skills/filmstack` then add a "filmstack" section to CLAUDE.md listing the available skills: /pitch-room, /coverage, /script-doctor, /market-comp, /logline, /series-bible, /pitch-deck, /breakdown, /casting-breakdown, /budget-review, /picture-lock, /adr-session, /dcp-delivery, /festival-strategy, /co-production, /press-kit, /taiwan-production, /rights-clearance, /wga-check, /retro.

### Add to a specific project

```bash
cp -Rf ~/.claude/skills/filmstack .claude/skills/filmstack
rm -rf .claude/skills/filmstack/.git
```

Then add to your project's `CLAUDE.md`:

```
## filmstack
Available skills: /pitch-room, /coverage, /script-doctor, /market-comp,
/breakdown, /casting-breakdown, /budget-review, /picture-lock,
/festival-strategy, /taiwan-production, /rights-clearance, /wga-check, /retro.
```

### Install as Cowork Plugin

filmstack is packaged as a Claude Cowork plugin. In Cowork, use the Plugin menu to install from the repository URL:



All 20 skills become available immediately as slash commands.

### Other agents (Codex, Gemini CLI, Cursor)

filmstack works on any agent supporting the [SKILL.md standard](https://github.com/anthropics/claude-code). Copy skills to `.agents/skills/filmstack/`.

---

## See it work

```
You:    I want to make a film about a Taiwanese tech billionaire who fakes his own death.
You:    /pitch-room

Claude: Before you write a word, six questions:
        1. What's the WOUND? Not the plot — the wound the character can't escape.
        2. Who does the audience root for when the billionaire is both villain and victim?
        3. What's the genre contract? Thriller promises resolution. Drama doesn't.
        4. What's the Taiwanese specificity that makes this NOT just another billionaire story?
        5. Who loses when he disappears — and do we care about them more than him?
        6. What does "faking death" COST him that money can't fix?

        [You answer. Claude synthesizes a creative brief.]
        [Brief is saved to .filmstack/creative-brief.md]

You:    /coverage script-draft-v2.pdf

Claude: TITLE: [Your Title]
        AUTHOR: [You]
        GENRE: Thriller / Drama
        PAGES: 112
        LOGLINE: A Taiwanese tech billionaire stages his own death to escape
                 a corruption investigation, only to discover the identity
                 he's running from is the only one worth keeping.

        SYNOPSIS: [Full 1-page spoiler synopsis]

        COMMENTS:
        CONCEPT: 8/10 — Premise is commercially viable. The Taiwanese setting
                 is underexploited in this genre...
        STRUCTURE: 6/10 — Act Two collapses around page 67...
        CHARACTER: 7/10 — Protagonist motivation is clear but antagonist is thin...
        DIALOGUE: 7/10 — Strong in confrontation scenes, expository in setup...
        MARKETABILITY: 8/10 — Strong streaming comp titles...

        RECOMMENDATION: CONSIDER
        [Detailed rationale]

You:    /script-doctor

Claude: IRON LAW: No fixes without diagnosis first.
        [Traces the Act Two collapse — 3 scenes that cause it]
        [Identifies the antagonist problem — missing scene on page 43]
        [Finds an unmotivated reversal on page 89]
        PROPOSED FIXES: [Specific, minimal, non-invasive]
```

---

## Docs

| Doc | What it covers |
|---|---|
| [Calibration Guide](CALIBRATION.md) | What filmstack can and cannot do — read this first |
| [Skill Deep Dives](docs/skills.md) | Philosophy and workflow for every skill |
| [Architecture](ARCHITECTURE.md) | Design decisions and pipeline logic |
| [Contributing](CONTRIBUTING.md) | How to add skills or improve existing ones |

## How filmstack works — and where it stops

filmstack skills divide into two tiers.

**Tier 1 — Institutional Knowledge:** Skills that encode verifiable industry standards — deal structures, union rules, funding frameworks, delivery specs, festival eligibility. The AI applies known frameworks to your specific situation. High confidence on the framework; always verify current rates and regulations against primary sources.

**Tier 2 — Creative Assessment:** Skills that work with aesthetic material — script structure, loglines, pitches, festival routing. These skills do not produce verdicts. They measure what is measurable, surface patterns that correlate with problems, and ask the questions a professional would ask. They prepare you for a human conversation. They do not replace it.

See [CALIBRATION.md](CALIBRATION.md) for a complete breakdown of what each skill can and cannot do.

**Development is not a pipeline.** The stage progression (Development → Pre-Production → ...) describes the order of production activities, not how development actually works. Real development is iterative: you loop between `/logline` and `/coverage` and `/script-doctor` as many times as the script requires. Use filmstack in the order the work demands, not in the order the table suggests.

**This is not a legal tool.** `/rights-clearance`, `/wga-check`, `/distribution-deal`, and `/music-licensing` produce preliminary analyses — they are not substitutes for qualified entertainment lawyers, labor consultants, or music supervisors. Always verify with professionals before production.

**Hollywood terminology** reflects US industry standards. `/taiwan-production` and `/korea-production` cover Asia-Pacific specifics. International co-productions will have different union agreements, clearance requirements, and distribution norms not covered by other skills.

## License

MIT. Free forever.
