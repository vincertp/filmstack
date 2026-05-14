# filmstack Calibration Guide

This document explains what filmstack can and cannot do — and why the distinction matters.

---

## The core problem with AI film tools

Most AI film tools pretend to know more than they do. They produce professional-looking outputs — script coverage, budget assessments, festival strategy — in the correct format, with the correct vocabulary, at confident volume. The format signals expertise. The expertise may not exist.

filmstack v2 is built around a different premise: **the value of a tool is proportional to its honesty about its own limits.**

---

## Two tiers of skills

filmstack skills divide into two tiers based on the type of knowledge required to produce reliable output.

---

### Tier 1: Institutional Knowledge Skills

These skills encode rules, standards, and frameworks that are:
- Largely verifiable against public sources
- Not primarily aesthetic or taste-based
- Stable over periods of months to years

**The AI's role:** Apply known standards to your specific situation. Flag deviations. Identify where professional consultation is required.

**Confidence level:** High for the framework; lower for jurisdiction-specific or rapidly-changing details. Always verify current rates and regulations with authoritative sources.

| Skill | What it knows reliably | What still requires a professional |
|---|---|---|
| `/distribution-deal` | MG structure, holdback norms, waterfall mechanics, predatory term patterns | Negotiation strategy, jurisdiction-specific law, current market conditions |
| `/music-licensing` | Two-license rule, PRO registration, cue sheet requirements, cost ranges by category | Specific clearance quotes, current licensing climate for specific songs |
| `/rights-clearance` | E&O pre-check categories, clearance types, common exposure areas | Actual legal opinion, defamation risk assessment |
| `/wga-check` | WGA/SAG-AFTRA minimums (verify current rates), residual triggers, credit arbitration rules | Whether a specific situation constitutes a violation |
| `/dcp-delivery` | SMPTE specs, KDM mechanics, delivery format standards | Specific theater requirements, current encryption standards |
| `/co-production` | Treaty framework, points test structure, general financial split requirements | Current treaty terms, specific bilateral negotiations |
| `/taiwan-production` | 文化部輔導金 categories, TAICCA structure, 國片認定 framework | Current cycle deadlines, reviewer priorities, specific eligibility questions |
| `/korea-production` | KOFIC program structure, national film points test, BIFF section descriptions, OTT platform comparison | Current application deadlines, current KOFIC review priorities |
| `/breakdown` | Industry-standard scene breakdown categories and format | Whether your specific production can execute a given breakdown |
| `/casting-breakdown` | Breakdown Express format and submission standards | Casting director relationships, current market for specific character types |
| `/budget-review` | Line item categories, cost-per-day norms by budget tier, red flag patterns | Local market rates, specific vendor quotes, current union minimums |
| `/picture-lock` | Post-production checklist, delivery spec categories | Specific platform delivery requirements (change frequently) |

---

### Tier 2: Creative Assessment Skills

These skills work with material that requires aesthetic judgment, taste, and accumulated human experience to evaluate reliably. filmstack v2 is honest about this: these skills do not produce verdicts. They produce structured analysis that prepares the writer for a more productive human conversation.

**The AI's role:** Measure what is measurable. Surface patterns that correlate with problems. Ask the questions a professional would ask. Not answer them.

**Confidence level:** High for mechanical observation. Medium for pattern inference. Low (not attempted) for aesthetic judgment.

| Skill | What it does reliably | What it explicitly cannot do |
|---|---|---|
| `/coverage` | Structural timing, scene metrics, pattern flag checklist, script-specific open questions | Assess voice, emotional resonance, cultural authenticity, or whether the story needs to exist |
| `/script-doctor` | Observe structural facts, flag patterns, surface questions | Diagnose why a character isn't compelling, whether a theme lands, or what this story is really about |
| `/logline` | Stress-test logline against known structural criteria (subject/verb/obstacle/stakes) | Determine whether the logline will actually sell the film |
| `/series-bible` | Structure a bible against industry format standards | Assess whether the story world is interesting or the characters are worth spending time with |
| `/market-comp` | Identify formal comparable titles by genre/budget/platform | Predict whether the market will actually receive your film the way the comps were received |
| `/pitch-deck` | Structure a pitch deck against investor/distributor expectations | Determine whether the pitch will land in a room |
| `/pitch-room` | Generate the questions a development executive would ask | Answer whether your concept is commercially viable |
| `/festival-strategy` | Map film against festival eligibility criteria and known programming patterns | Predict acceptance, or know who the programmer will be when you submit |

---

## The non-linearity of development

filmstack presents a pipeline:

```
Development → Pre-Production → Production → Post-Production → Distribution
```

Real development is not a pipeline. It is a loop.

You write a logline. You run `/pitch-room`. The questions reveal that you haven't figured out the wound. You rewrite the logline. You write a draft. You run `/coverage`. The structural analysis reveals that Act Two has the protagonist making no choices. You run `/script-doctor`. You discover that the protagonist's want from Act One never resolved. You rewrite the want. Now the logline is wrong. You return to `/logline`.

**Use filmstack iteratively, not sequentially.** The pipeline is a description of the eventual order of production activities — not a description of how development actually works.

---

## filmstack as pre-meeting preparation

The best use of filmstack is not to replace human professional feedback. It is to make the human professional's time more valuable.

Before sending a script to a reader: run `/coverage` to catch the structural problems you could catch yourself. Use the open questions as your own pre-read.

Before a distribution negotiation: run `/distribution-deal` to understand the standard terms and flag the non-standard ones.

Before meeting with a Korean co-producer: run `/korea-production` to know the KOFIC points test before they assume you do.

Before pitching at a market: run `/pitch-room` to answer the forcing questions before a development executive asks them with real consequences.

filmstack gives you the institutional knowledge to show up to those conversations prepared. The conversations still need to happen.

---

## When filmstack will be wrong

**Union rates and delivery specs change.** SKILL.md files encode rates as of their version date. Always verify current minimums against official sources (wga.org, sagaftra.org, KOFIC's current application guide, your target platform's current delivery spec).

**Creative assessments reflect training patterns, not universal taste.** When `/coverage` flags a structural pattern, it is applying norms from mainstream commercial filmmaking. If your film deliberately breaks those norms, the flag is not wrong — but the interpretation is up to you.

**International legal frameworks evolve.** Co-production treaties change. Tax incentives change. OTT commissioning priorities change. filmstack is a starting framework, not a current legal opinion.

**The AI can be confidently wrong.** This is the nature of language models. When filmstack produces output that sounds authoritative but doesn't match your research from primary sources, trust the primary sources.

---

## Version history

| Version | Change |
|---|---|
| v1.0.0 | Initial release. All skills produced professional-format outputs with verdict-level confidence. |
| v2.0.0 | Redesigned creative assessment skills (coverage, script-doctor) with explicit epistemic tiers. Added CALIBRATION.md. Added confidence field to all SKILL.md frontmatter. Clarified Tier 1 vs. Tier 2 skill design. |
