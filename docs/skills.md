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

---

## /logline

**Role**: Story Consultant (Logline Specialist)

**Philosophy**: A logline is not a summary — it is a sales instrument. The discipline of writing a strong logline forces a kind of clarity that cannot be faked: if you cannot describe your film in one sentence that creates curiosity, you don't fully know what your film is yet. `/logline` weaponizes this discipline.

**The five failure modes**: The skill is structured around five specific ways loglines fail (plot summary, theme statement, missing stakes, generic protagonist, missing antagonist logic). This taxonomy is more useful than general advice because it gives the writer a specific diagnosis — "your logline is a theme statement" is actionable in a way that "your logline isn't working" isn't.

**Three candidates**: The skill produces three versions (genre-forward, character-forward, stakes-forward) rather than one "correct" logline. This is intentional: different pitching contexts favor different framings. A studio pitch favors genre clarity; a festival programmer pitch may favor character specificity.

**The 40-word limit**: Industry standard for pitch loglines. Elevator pitches are literally that — the time it takes an elevator to go between floors. If the logline can't be said aloud in under 20 seconds, it fails in practice regardless of how good it reads on paper.

**Output**: Appends logline candidates to `.filmstack/creative-brief.md` — the shared context document that all development-phase skills read.

---

## /series-bible

**Role**: TV Writer / Showrunner

**Industry context**: A series bible is the foundational document for pitching a television series. It is longer and more detailed than a pitch deck, denser than a treatment, and distinct from a pilot script. Networks, streamers, and production companies use the bible to assess whether a concept has series potential — whether the world is rich enough, the characters complex enough, and the conflicts renewable enough to sustain multiple seasons.

**Format determines everything**: The bible requirements differ significantly between broadcast, cable, and streaming. Broadcast requires a procedural element (something resolved each week); streaming tolerates fully serialized storytelling; limited series doesn't need to prove ongoing potential. `/series-bible` establishes format first and adjusts requirements accordingly.

**The five bible killers**: The most important diagnostic function of the skill. "The Feature Trapped in a TV Show" — a story that resolves everything in 90 minutes — is the most common development problem for writers transitioning from film. A biblical killer identified before pitching saves months of wasted development.

**Ongoing potential section**: The clearest test for whether a concept is truly a series concept. If Season 2 cannot be described convincingly in a paragraph, the concept may be a limited series or a film. This is not a failure — it is a clarification that allows the writer to pitch the right format.

**Output**: Saves to `.filmstack/series-bible-[date].md`. Version by date — the bible evolves throughout development.

---

## /pitch-deck

**Role**: Story Executive / Packaging Specialist

**Industry context**: The pitch deck is the document that gets you in the room — and the document that keeps you out of it if it's wrong for the audience. A deck designed for a studio executive looks different from a deck for a private equity investor, which looks different from a deck for an international co-production partner. `/pitch-deck` establishes audience first.

**The deck vs. the bible**: The most important distinction in development documentation. A series bible is a writer's document — dense, specific, intended for people who need to understand the show deeply. A pitch deck is a sales document — visual, selective, intended for people deciding whether to take a second meeting. Confusing the two is a common and expensive mistake.

**The nine slides**: The structure (Hook → Logline → Story → Why Now → Characters → Visual World → Comps → Team → Ask) is designed around the psychology of a pitch meeting. The hook creates curiosity before the buyer knows anything about the project. The "Why Now" slide answers the question every buyer is implicitly asking: why should this get made now, on my slate, with my resources?

**The Ask slide**: The most commonly weakened slide in independent film pitch decks. "We're looking for partners" is not an ask — it is an invitation to be ignored. Specific asks ("$2.4M for 50% equity") communicate preparation and seriousness. Vague asks communicate inexperience. The skill consistently pushes for specificity on this slide.

**Visual execution note**: `/pitch-deck` produces the content structure and copy. Visual design — layout, typography, image selection — requires a human designer. The skill is explicit about this boundary.

**Output**: Saves to `.filmstack/pitch-deck-[date].md`. The deck itself requires design software (Keynote, PowerPoint, Google Slides, Canva) — the skill outputs the content and structure.

---

## /co-production

**Role**: International Co-Production Consultant

**Industry context**: International co-production is one of the most misunderstood concepts in independent film financing. Most productions that call themselves "co-productions" are actually co-financings — money from multiple countries, but the film is only "domestic" in one. The distinction matters enormously for subsidy eligibility, tax credits, and distributor obligations.

**The points test**: Most bilateral treaties use a points system that assigns weighted values to key creative roles based on nationality. A director is typically worth 3 points, a lead actor 2 points. If the creative team is dominated by one nationality, treaty qualification requires deliberate casting and hiring decisions — which can create tension with purely creative choices.

**Treaty status verification**: The skill explicitly warns that treaty status changes with diplomatic relations. China-Canada and China-Australia treaties have both been affected by geopolitical developments. No skill can substitute for verifying current treaty status with the administering body (CAVCO, BFI, Screen Australia, KOFIC) at the time of the deal.

**Taiwan note**: Taiwan has a limited bilateral treaty network. Most "Taiwan co-productions" are technically co-financings — a distinction that affects TAICCA subsidy eligibility and how the film is classified in each territory.

**Output**: Saves to `.filmstack/co-production-[date].md`. The explicit disclaimer that entertainment counsel is required in all territories is non-removable.

---

## /adr-session

**Role**: Post-Production Sound Supervisor

**Industry context**: ADR (Automated Dialogue Replacement) is one of the most preparation-dependent sessions in post-production. An actor in an ADR studio watching themselves onscreen from six months ago, trying to match lip movements, emotional performance, and acoustic environment simultaneously, in a dead-acoustic isolation booth — this is technically and emotionally demanding work. Preparation determines whether the session produces usable material or expensive pickups.

**The cue sheet as the session**: The ADR cue sheet is the session. Every ambiguity in the cue sheet (wrong scene number, missing timecode, unclear line change) costs time in the studio. The skill is built around producing a complete, unambiguous cue sheet before any talent is booked.

**Line changes and WGA**: Any dialogue change from the original script on a WGA production requires writer approval. This is not optional. The skill flags line changes explicitly because they are easy to overlook during the speed of post-production and expensive to discover after the session.

**Director presence rule**: The skill explicitly states that the director must be in the ADR session and that the session should be rescheduled if they cannot attend. This is because ADR performance decisions require directorial judgment — a sound supervisor cannot approve a performance as a substitute for the director.

**Output**: Saves to `.filmstack/adr-session-[date].md`. The cue sheet format is designed to be used directly in the studio session.

---

## /dcp-delivery

**Role**: Digital Cinema Delivery Specialist

**Industry context**: A DCP (Digital Cinema Package) is not a video file. It is an encrypted, format-specific package that can only be played by DCI-compliant projectors with the correct KDM for that specific projector, on that specific date. The technical requirements are exact, the deadlines are hard, and the consequences of getting it wrong at a festival premiere are irreversible.

**The KDM system**: KDMs (Key Delivery Messages) are time-locked decryption keys specific to individual projectors. A KDM that expires at 23:59 cannot play a screening that begins at 23:45 and runs past midnight. KDM validity dates are among the most common causes of screening failures at festivals. The skill builds KDM management — collecting projector certificates, generating KDMs with correct validity windows, confirming delivery — into the checklist explicitly.

**Drive format**: ext2/ext3 filesystem for physical delivery, not NTFS or macOS Extended. Most DCP servers run Linux. This is the second most common cause of premiere-day failures. The skill states it explicitly because it is easy to format a drive in whatever the operating system defaults to.

**QC at the venue**: A DCP that has not been QC'd on the actual projector has not been delivered. The skill defines "delivery complete" as "the projectionist has confirmed ingest, KDM load, and test playback" — not as "we shipped the drive."

**Output**: Saves to `.filmstack/dcp-delivery-[date].md`. The delivery schedule section tracks each venue independently because each projector requires its own KDM.

---

## /press-kit

**Role**: Unit Publicist / Festival Submissions Coordinator

**Industry context**: A press kit is a working document for journalists and programmers — not a vanity package for the production. The distinction matters because productions tend to write press kits for themselves (celebrating the film they made) while journalists and programmers read press kits for information (what is this film, why should I care, what do I need to write about it or screen it).

**Submission EPK vs. full press kit**: The skill distinguishes clearly between these two different documents. Festival submission EPKs should be minimal — a 40-page press kit sent to a festival submission inbox will not be read. Full press kits for press and distributors need to be complete. The skill handles both, and asks the user to identify which they need before building.

**Stills approval**: The most commonly missed element in independent film press kits. SAG-AFTRA productions and many actor contracts require individual still approval before publication. Releasing un-approved stills creates legal exposure and damages relationships with talent representation. The skill makes stills approval status a required field, not an optional one.

**Director statement failures**: The skill identifies specific failure patterns for director statements — the most common being a statement that describes what the film is about rather than why the director made it. Programmers read director statements to understand the filmmaker's intent and voice. A statement that sounds like a synopsis is a missed opportunity to create a human connection with the programmer.

**Output**: Saves to `.filmstack/press-kit-[date].md`. Version control is important — the submission EPK, selected film kit, and theatrical kit are different documents at different stages.

---

## /taiwan-production

**Role**: Taiwan Production Consultant

**Philosophy**: 台灣電影產業的補助邏輯與好萊塢的工會義務體系截然不同。文化部輔導金是申請制政府補助，有明確截止日、競爭性審查，以及文化價值評估維度；這跟 SAG-AFTRA 最低工資義務（一旦觸發就必須遵守）的運作邏輯完全不同。`/taiwan-production` 不是其他 skills 的「翻譯版」，而是獨立的知識域，處理台灣製作環境特有的問題。

**國片認定的核心作用**: 通過國產電影片認定是申請文化部輔導金的前提條件，但認定條件（創作人員國籍比例、資金來源）可能與國際合製的需求產生張力。Skill 把這個張力明確點出，讓製作人在結構合製方案時就預見潛在問題。

**TAICCA 投資 vs. 補助的區別**: 這是台灣業界常見的混淆點。TAICCA 的文化內容投資基金是「投資」（有退場機制、需還本分潤），不是「補助」。`/taiwan-production` 把兩者的性質差異說清楚，避免製作人誤以為拿到 TAICCA 資金就等同於政府補助。

**金馬與國際影展的時序策略**: 金馬影展希望台灣電影優先在台灣有首映機會，這與走 Sundance / Berlin 等大展的國際策略有潛在衝突。Skill 把這個張力作為策略考量點提出，而非規定答案——因為正確選擇取決於每個計畫的具體目標。

**Output**: 儲存至 `.filmstack/taiwan-production-[date].md`。內容以繁體中文書寫，符合台灣業界的工作語言習慣。
