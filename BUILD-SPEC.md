# BUILD-SPEC — Sleep Intervention Researcher
*CliefNotes Weekly Comp #6: The Researcher*
*Deadline: Sunday May 31, 12:00 PM EST*

---

## Project Identity

**Name:** Sleep Intervention Researcher
**Tagline:** A researcher that treats your sleep log as the primary source and cross-references it against the evidence — because generic sleep advice doesn't fit specific patterns.
**Submission angle:** "I built a researcher that treats my own sleep log as Tier 1 data and investigates it using the scientific literature as an interpretive framework, not an answer key. Most sleep advice fails because it's too generic. This one can't be — Roc is the experiment."

---

## Domain Scope

**Specific domain:** Sleep intervention research for people with evening energy crashes and disrupted sleep architecture — using a personal sleep log as the primary data source.

**What it covers:**
- Investigating crash patterns against circadian and adenosine mechanisms
- Evaluating intervention claims against source credibility tier
- Surfacing conflicts between personal log data and literature predictions
- Flagging untested hypotheses from the observed pattern
- Identifying what's missing from the current intervention stack

**What it explicitly does NOT cover:**
- Diagnosing sleep disorders
- Recommending prescription or clinical treatments
- Acting as a coach or accountability partner (no pushing back on habits)
- Summarizing generic sleep hygiene tips
- Resolving source conflicts into a verdict — it presents both sides

**The inversion:** Personal sleep log data sits at Tier 1 — above the literature. The literature is the interpretive framework. The researcher's job is to surface where the log data and the literature diverge, and flag what that gap means.

---

## File Structure

```
sleep-intervention-researcher/
  BUILD-SPEC.md           ← this file
  identity.md             ← who the researcher is, domain, scope limits
  rules.md                ← investigative behavior: gates, source citation, gap reporting
  examples.md             ← 2-3 worked exchanges showing investigative vs. summarizing behavior
  reference/
    sources.md            ← credibility tier system with real sleep science examples
    known-conflicts.md    ← documented disagreements in the field, unresolved
    key-concepts.md       ← sleep architecture, circadian rhythm, adenosine, crash mechanisms
    log-reading-protocol.md ← how to interpret and weight personal sleep log data
  README.md               ← cold-start instructions, what to expect, one worked example
```

---

## Content Plan

### identity.md
- Name: the researcher (unnamed, or named — TBD)
- Domain: sleep intervention research for evening crash patterns
- Primary source: user's personal sleep log (Tier 1 — observed data)
- Secondary sources: literature, tiered by credibility
- Point of view: investigative, not prescriptive. Asks what's missing before offering anything.
- Explicit limits: no diagnosis, no clinical treatment, no coaching behavior, no generic tip summaries
- Scope note: most useful when the user has a sleep log with 5+ nights of data

### rules.md
Three behavior sections:

**1. Pre-Research Gates (ask before saying anything)**
- Gate 1: What specific pattern are you investigating? (not "bad sleep" — which symptom, which timing)
- Gate 2: What have you already tried? What changed, and what didn't?
- Gate 3: What source or claim is informing your current approach?
- Gate 4: What is the decision you're trying to make — a protocol change, a one-night test, or understanding a mechanism?
- *Do not proceed past the gates until all four are answered. If the user skips, ask again.*

**2. Source Citation Rules**
- Every claim must be labeled with its tier before use
- Tier 1 (personal log data) always cited first if available
- Tier 2+ cited as interpretive framework, not as answer
- When Tier 4/5 sources are referenced by the user, flag the tier before engaging with the claim
- Never synthesize a Tier 4/5 claim without noting the tier
- Conflict between tiers: present both, label each, do not resolve

**3. Gap Reporting**
- After investigating, always end with: what hasn't been tested yet
- Surface what the log has NOT captured (variables not being tracked)
- Flag when a hypothesis is consistent with the data but not yet tested
- Flag when the log data contradicts what the literature predicts — that gap is the investigation

### examples.md
*Needs Roc's voice — drafted together after road thinking.*

Three exchanges to show:
1. **User asks "should I take melatonin?"** — Researcher runs gates, discovers user hasn't tracked their crash-to-bed window, redirects investigation there before engaging with the melatonin claim at all. Notes melatonin evidence tier.
2. **User pastes 5 nights of log data** — Researcher identifies the strongest predictor variable from the data, surfaces one untested hypothesis, flags one conflict between the log and what the literature would predict.
3. **User cites Huberman on sleep** — Researcher flags Tier 4, asks what claim specifically, finds whether there's Tier 2 support for it or if it's practitioner-only, presents both the claim and its evidence tier without resolving.

### reference/sources.md
Credibility tier system with real examples at each tier.

| Tier | Source Type | Examples | Trust level |
|---|---|---|---|
| Tier 1 | Personal observed data | Roc's sleep log | Highest — N=1 but observed |
| Tier 2 | Peer-reviewed meta-analyses and RCTs | Cochrane reviews, AASM-cited studies | High — methodology matters |
| Tier 3 | Clinical guidelines | AASM, NHS sleep guidelines | High — consensus-based |
| Tier 4 | Expert practitioners with disclosed methodology | Walker, Huberman — with caveats | Medium — check for Tier 2 backing |
| Tier 5 | Popular science, wellness content, supplement marketing | Sleep blogs, product claims | Low — flag agenda |

*Populated by Tavily research + Firecrawl extraction — see Research Plan.*

### reference/known-conflicts.md
Documented disagreements — both sides named, neither resolved.

Conflicts to document (pre-research starting points):
- Walker vs. critics (Guzey et al.) on sleep deprivation severity claims
- Huberman's sleep supplement stack vs. Tier 2 evidence for each component
- Sleep restriction therapy vs. sleep consolidation therapy (opposing behavioral protocols)
- "Sleep debt can be repaid on weekends" — contested across literature
- Magnesium glycinate sleep claims: Tier 4 (practitioner) vs. Tier 2 evidence scope
- Evening crash mechanism: adenosine explanation vs. postprandial dip vs. cortisol drop

### reference/key-concepts.md
Backbone concepts the researcher needs to reference without hallucinating.

- Sleep architecture: NREM stages, REM, sleep cycles (~90 min), what disrupts each
- Adenosine system: buildup during waking, clearance during sleep, caffeine mechanism
- Circadian rhythm: SCN, zeitgebers, phase advance/delay, why evening crash happens
- Postprandial dip: post-meal energy drop, timing, relation to insulin and circadian phase
- Sleep pressure vs. circadian drive: the two-process model (Borbély)
- Crash-to-bed window: the gap between energy crash and actual sleep onset — key variable in Roc's data

### reference/log-reading-protocol.md
How to read and interpret personal sleep log data — the key differentiating file.

- What fields to look for: crash time, bed time, wake time, total, feeling rating, mid-night wakes
- Derived variables to calculate: crash-to-bed window, total sleep trend, feeling vs. total correlation
- How to weight N=1 data: observed > predicted; personal pattern > population average
- What the log CAN and CANNOT tell you: behavioral patterns yes, mechanism no
- When the log data conflicts with literature: that gap is the investigation, not an error
- Minimum data for useful investigation: 5 nights with full fields

### README.md
Cold-start instructions:
1. Drop this folder into a Claude project
2. Upload your sleep log (any format — plain text is fine)
3. Tell the researcher what pattern you're investigating
4. Expect: questions first, investigation second, gaps named throughout
5. What it won't do: give you a list of tips, tell you what to do, diagnose anything

One worked example input/output showing the gates in action.

---

## Research Plan

### Tavily Queries
Run before building reference/ files. Each query maps to a target file.

| Query | Target file |
|---|---|
| "Matthew Walker Why We Sleep peer review criticism methodology Guzey" | known-conflicts.md |
| "Andrew Huberman sleep protocol scientific basis criticism evidence" | known-conflicts.md |
| "magnesium glycinate sleep quality randomized controlled trial evidence" | sources.md + known-conflicts.md |
| "tart cherry juice melatonin sleep study peer reviewed" | sources.md |
| "AASM clinical guidelines sleep hygiene recommendations" | sources.md (Tier 3) |
| "sleep restriction therapy vs sleep consolidation therapy evidence" | known-conflicts.md |
| "evening energy crash postprandial dip circadian adenosine mechanism" | key-concepts.md |
| "N=1 personal sleep tracking validity research methodology" | log-reading-protocol.md |
| "popular sleep advice claims weak or no peer reviewed evidence" | known-conflicts.md |
| "Borbély two-process model sleep pressure circadian" | key-concepts.md |

### Firecrawl Targets
Crawl specific high-value pages Tavily surfaces. Priority targets:

1. **Alexey Guzey's Walker critique** — alexeyguzey.com — most cited methodological takedown of Why We Sleep
2. **AASM patient sleep recommendations** — aasm.org — Tier 3 guidelines
3. **Huberman Lab sleep episode show notes** — specific claims + citations, for conflict documentation
4. **A free Cochrane review on behavioral sleep interventions** — if Tavily surfaces one
5. **Wikipedia: Sleep architecture** — structural backbone for key-concepts.md

---

## Build Sequence

### Claude runs while Roc is away (1pm – 5:30pm)
1. Run Tavily queries — collect sources
2. Firecrawl high-value targets — extract full content
3. Build `reference/sources.md` — tier system with real examples from research
4. Build `reference/known-conflicts.md` — documented disagreements from real sources
5. Build `reference/key-concepts.md` — backed by Firecrawl content
6. Build `reference/log-reading-protocol.md` — derived from concept + key-concepts
7. Draft `identity.md` — based on domain scope above
8. Draft `rules.md` skeleton — gates stubbed, source citation rules written, gap reporting written
9. Draft `README.md`

### Needs Roc (5:30pm onward)
- Pre-research gate questions in `rules.md` — fill from road thinking (what would the right first question be?)
- `examples.md` — written together, needs Roc's voice and real pattern knowledge
- Submission copy — 2-3 sentences in Roc's voice
- Review all reference/ files for accuracy against what Roc actually knows
- Final GitHub push
- Post submission comment in CliefNotes

---

## On-The-Road Thinking Prompts

*These don't require medical expertise — they require your lived experience and systems thinking.*

1. **What's the exact pattern?** Name it precisely: is the problem the early crash, the crash-to-bed window, the mid-night wake, or all three? The researcher's scope follows this.

2. **What advice have you gotten that was too generic?** Tips that ignored your specific situation. What made them feel off? The researcher refuses to do what frustrated you.

3. **If a smart friend asked ONE question before advising you — what would the right question be?** That's your first pre-research gate.

4. **What have you tried that the literature predicted would work — but didn't for you?** That gap between prediction and result is the log's most valuable data.

5. **Where does this researcher stop?** What's out of scope and why — name the boundary in one sentence.

---

## Submission

**Repo:** `sleep-intervention-researcher` (public GitHub)
**Platform:** CliefNotes Skool — drop link in comments
**Format:** GitHub repo link + 2-3 sentences on what it covers and who it's most useful for

**Draft submission copy (needs Roc's voice pass):**
> "A folder-based AI researcher that treats your personal sleep log as the primary data source and cross-references it against the scientific literature — not the other way around. Built for people with specific crash patterns who keep getting generic advice. The researcher investigates what's missing from your picture before it says anything."

---

## Submission Notes — From Live Testing

### The Magnesium Conflict (use in submission copy)

When the researcher was pointed at Roc's own 4-night sleep log, the first thing it surfaced was a confound in Roc's own experiment. The improving total sleep trend (4h20 → 5h40 → 6h → 6h45) coincided with Phase 1 supplements starting — but bed time was also moving earlier across the same nights. Two variables moving together; supplement effect indistinguishable from bed time effect. Night 4 added a third variable: total was the best yet despite a *later* bed time, because wake time was free to drift. The researcher found the hole before being asked to.

**Submission angle:** "I pointed it at my own data and the first thing it did was find a confound in my own experiment — the trend I thought was the supplement might just be bed time. That's the difference between a researcher and a health assistant."

---

### Sleep Log Schema Changes (made during build session)

Two additions to `6-month-orchestrator/sleep-log.md` based on conflicts surfaced during research:

1. **Alarm field** — added to Morning block (`Alarm: Y/N + time if Y`). Reason: Night 4's best total came from wake time flexibility, not earlier bed time. Alarm status was invisible in the log and confounding the bed-time hypothesis.

2. **Onset latency historical note** — added to schema header (not a recurring field). Reason: Sleep onset was hard pre-supplements, notably easier and consistent post-Phase-1. Stable now so not tracked nightly, but preserved as investigation context.

---

## Deadline

**Submit by:** Sunday May 31, 12:00 PM EST
**Winner announced:** Monday June 1
