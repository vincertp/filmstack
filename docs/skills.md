# Skill Deep Dives

Complete reference for every filmstack skill — philosophy, workflow, and industry context.

---

## /pitch-room

**Role**: Story Executive / YC-style development session

**Philosophy**: The most expensive mistake in film development is building on a broken foundation. `/pitch-room` exists to find the foundation problems before they become scripts, and scripts before they become productions. The six forcing questions are not warm-up questions — they are diagnostic tools designed to expose the weakest point in a concept.

The structure is borrowed from Y Combinator's office hours philosophy: ask the questions nobody else is willing to ask, in the room where the founder still has time to change course.

**Key behavior**: The skill is explicitly instructed not to validate. It is specifically told to push back on vague answers. This is unusual — most AI tools default to encouragement. `/pitch-room` defaults to honest challenge.

**Output**: Creates `.filmstack/creative-brief.md`, which becomes the shared context document for all downstream skills. If you skip `/pitch-room`, consider creating this file manually — other skills read it.

---

## /coverage

**Role**: Script Reader (professional, production company / studio)

**Industry context**: Script coverage is the gating mechanism of Hollywood development. Every script submitted to a production company, studio, or streaming platform is first read by a script reader whose coverage determines whether anyone higher in the organization sees it. A PASS from a reader means the script is dead — the executive will likely not read it.

The Pass/Consider/Recommend system is universal across the industry. A Recommend is extraordinary — experienced readers may give only a handful per year.

**Key behavior**: The skill explicitly instructs the AI to write for the buyer, not for the writer. This produces accurate, useful coverage rather than encouraging notes.

**Coverage format specifics**:
- Logline: Maximum 40 words, does not spoil the ending
- Synopsis: 1 page maximum, full spoilers, present tense — this is internal to decision-makers
- Comments: 5 dimensions scored 1–10 with specific page citations
- Recommendation: Includes specific rationale for what would change the rating

**Output**: Saves to `.filmstack/coverage-[date].md`. Version by date — multiple drafts can coexist.

---

## /script-doctor

**Role**: Story Editor

**Philosophy**: The Iron Law — no fixes without diagnosis — is the most important constraint in this skill. The most common failure mode in script development is prescribing solutions before understanding root causes. A story editor who says "the second act needs more tension" has diagnosed a symptom. A story editor who says "the second act loses momentum because on page 67 the protagonist stops actively pursuing their want and instead reacts to events — tracing back to an unmotivated reversal on page 54 that undermines the end-of-Act-One decision" has diagnosed a cause.

**Key behavior**: The skill maps the story skeleton first (all major structural beats with page numbers) before identifying any problems. This prevents premature diagnosis.

**Principle of minimum intervention**: The smallest fix that solves the problem is the right fix. This is clinically correct (rewrites introduce new problems as often as they solve old ones) and practically useful (smaller fixes are more likely to be implemented).

**Relationship to /coverage**: `/script-doctor` reads coverage from `.filmstack/` before forming its own assessment. This ensures continuity and prevents the frustrating experience of getting the same notes from two different sources.

---

## /market-comp

**Role**: Development Executive (packaging/sales)

**Industry context**: Comparable titles serve two different functions in Hollywood:
1. **Communication tool** (primary): Tells buyers what drawer to put the project in
2. **Research tool** (secondary): Provides budget benchmarks and audience data

filmstack uses comp titles for both, while explicitly warning against the third misuse — letting comps drive creative decisions.

**"A meets B" format**: This is standard industry pitch shorthand. The formula communicates genre + tone in two data points. One title carries the world/concept; the other carries the emotional register. "*Parasite* meets *Knives Out*" says: Korean social satire + crowd-pleasing thriller mechanics. Both titles must be from the last 5–7 years — older comps signal the developer isn't current.

**Budget tiers**: The four-tier system (micro/low/mid-range/studio) maps to the actual financing universe for independent films. Each tier has different buyer pools, distribution paths, and union agreements.

---

## /breakdown

**Role**: First Assistant Director

**Industry context**: Script breakdown is the most detailed and painstaking document in pre-production. In professional production, breakdown is done by the 1st AD in collaboration with the production coordinator. Every element that must be sourced, hired, or rented is extracted from the script — if it's in the script and not in the breakdown, it will not be budgeted and will not be available on shoot day.

**Page count in eighths**: The film industry measures script pages in eighths (one page = 8/8). A 3/8-page scene is a scene that runs slightly under half a page. This precision matters for scheduling — it's the difference between a scene that fits in half a day and one that takes three-quarters of a day.

**Flags**: Red flags are not stylistic concerns — they are production cost and complexity multipliers. A night exterior sequence doesn't just mean "harder" — it means additional lighting equipment, potential overtime, and possible location constraints that don't apply during the day. Identifying flags early allows the production to plan around them or negotiate script changes.

---

## /casting-breakdown

**Role**: Casting Director

**Industry context**: Casting breakdowns are submitted to talent agencies via Breakdown Express (the industry standard platform). This is how professional actors and their representatives find out about available roles. The breakdown is the first communication between a production and the talent community.

**Inclusivity in breakdowns**: The industry has shifted significantly toward inclusive casting practices. Current best practice is to limit physical descriptions to characteristics that are genuinely essential to the story. A breakdown that specifies unnecessary physical characteristics narrows the talent pool arbitrarily and may signal to the talent community that the production is not interested in diversity.

**Coogan Law**: Named after Jackie Coogan, this California law requires that a portion of a child actor's earnings be set aside in a trust and that the production provide various protections. Most US states have equivalent laws. Every scene with an actor under 18 requires specific planning.

---

## /budget-review

**Role**: Line Producer

**Industry context**: Line producers are the financial managers of productions. They are responsible for everything below-the-line — crew, equipment, locations, and all production costs — and they are personally accountable if the production goes over budget. A good line producer's primary skill is seeing cost problems before they happen.

**Above-the-line vs. below-the-line**: This division is specific to film and television budgeting:
- Above-the-line (ATL): Writer, director, producers, principal cast — "creative" elements
- Below-the-line (BTL): Crew, equipment, locations, production costs — "technical" elements

ATL costs are typically negotiated; BTL costs are more predictable and form the core of a detailed budget.

**SAG-AFTRA agreements**: Union minimums create the pricing floor for union productions. The Ultra Low Budget Agreement, Modified Low Budget, Low Budget, and Basic Agreement have progressively higher minimums. Choosing the wrong tier — or not knowing which tier applies — is a common and expensive mistake.

---

## /picture-lock

**Role**: Post-Production Supervisor

**Industry context**: "Picture lock" is the moment the edit is finalized. After picture lock, the sound department can start the final mix, the VFX department delivers finals, and color grading begins. If the picture changes after lock — a re-open — it invalidates downstream work and costs money.

**M&E track**: The Music & Effects (M&E) track is a separate audio mix with all music and effects but no dialogue. It is required for every international distribution sale — foreign distributors need a clean audio bed to add dubbed dialogue. If an M&E track was not created during the original mix, it is extremely difficult and expensive to create afterward. This is one of the most commonly overlooked deliverables on independent productions.

**Closed captions**: Required by US law (ADA) for streaming platforms. Required in many international territories. Cannot be waived. Plan for them.

---

## /festival-strategy

**Role**: Sales Agent / Festival Strategist

**Industry context**: The festival circuit is a market. Films are positioned, packaged, and sold at festivals. Prestige matters, but strategic fit matters more — a Sundance slot is worthless to a film that needs a genre audience, and Fantastic Fest is useless to an art film seeking European distribution.

**Premiere status**: The concept of world premiere, international premiere, and North American premiere is critical for festival strategy. Major festivals require or strongly prefer premiere status. A film that screens anywhere publicly — including informal test screenings or crowdfunder rewards — may lose premiere eligibility. This must be managed proactively.

**Volume vs. selectivity**: 120–180 festival submissions is the industry guidance for a full run. This is expensive and time-consuming. Selective strategies (fewer, better-targeted submissions) work better for some films; volume strategies (maximize chances) work better for others. The right strategy depends on the film's goal.

---

## /rights-clearance

**Role**: Entertainment Rights Consultant

**Industry context**: E&O (Errors & Omissions) insurance is required by virtually every distributor before distribution. E&O insurance requires a clean chain of title and documented clearance of music, life rights, and other potential claims. A film that cannot obtain E&O insurance cannot be distributed through mainstream channels.

**Music clearance**: The most common and most expensive clearance problem. Two separate licenses are required for every recorded track — synchronization (the composition) and master use (the specific recording). These come from different parties who may not cooperate with each other or may charge prohibitive fees. "Public domain" music requires careful verification — the composition may be public domain while the specific recording is still under copyright.

**Life rights**: Real persons depicted in a film have privacy and publicity rights. A life rights agreement from a living person provides a contractual defense against many (but not all) claims. It does not prevent lawsuits — it provides grounds for defense.

---

## /wga-check

**Role**: Labor Compliance Consultant

**Industry context**: WGA and SAG-AFTRA membership obligations "attach" to productions based on specific triggers. A production company that doesn't know the triggers can accidentally become obligated to an agreement they weren't planning to sign — creating significant financial and contractual obligations.

**Student film exemption**: Film school productions by enrolled students for academic credit are generally exempt from WGA and SAG-AFTRA jurisdiction. The exemption has conditions and does not apply to productions that begin life as student films but are later developed commercially.

**Residuals**: Residuals are payments made to writers and actors on exploitation of the film after initial release — streaming replays, home video, broadcast. They are calculated formulas in the guild agreements. They must be budgeted as a production obligation, even on low-budget productions, because they attach regardless of whether the production has the cash to pay them at the time of distribution.

---

## /retro

**Role**: Producer

**Philosophy**: A retrospective that produces vague recommendations is worse than no retrospective. "Communication could be better" teaches nothing. "The location was scouted 3 days before the shoot, leaving the 1st AD no time to adjust the schedule for the discovered power access limitation — next time, lock all locations 14 days before shoot" is a retrospective that produces change.

**Phase retrospectives**: filmstack recommends running `/retro` at the end of each major production phase, not just at project completion. A development retro before pre-production catches mistakes while they can still be addressed. A production retro at wrap provides data while everyone's memory is fresh.
