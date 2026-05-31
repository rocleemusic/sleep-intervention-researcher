# Paused — Sleep Intervention Researcher v1
*Status as of May 31, 2026. Do not execute — reference only.*

---

## What's Done

- `reference/sources.md` — tier system, real named examples, Walker/Huberman caveats
- `reference/known-conflicts.md` — 6 conflicts documented, unresolved
- `reference/key-concepts.md` — 6 core concepts, crash-to-bed window populated with Roc's data
- `reference/log-reading-protocol.md` — complete including first-contact protocol
- `identity.md` — complete
- `rules.md` — source citation + gap reporting complete; gates stubbed (Gate 1 has raw notes)
- `README.md` — complete with worked first-message example
- `BUILD-SPEC.md` — submission notes section added (magnesium conflict story + log schema changes)
- `sleep-log.md` — alarm field added to Morning block schema; onset latency historical note added

---

## To Finish v1 (In Order)

### Step 1 — Fill gate questions in `rules.md`
Roc's job. Gate 1 has raw brainstorm notes — these need to become single, precise questions the researcher actually asks. Before writing them, read `reference/claude-research.md` Q4 (the 8 pre-intervention questions). That's the professional model the gates are approximating. Each gate = one sentence, written as the exact question the researcher would ask out loud.

Current Gate 1 notes to work from:
- "are you going to bed at the same time every night" — too generic; reframe toward crash-to-bed window
- "are you thinking too much / stressed" — outside scope; researcher doesn't do hyperarousal assessment
- "are you having a hard time going to sleep" — now answered historically (onset improved with supplements); not the right gate for this pattern

The gates should be scoped to the specific crash-to-bed window pattern this researcher is built around, not generic insomnia intake questions.

---

### Step 2 — Add valerian to `reference/known-conflicts.md`

New conflict entry needed. Key points to cover:
- The subjective/objective dissociation: people feel better; PSG shows no consistent change in any objective measure (sleep efficiency, time in stage, onset latency) across 16 RCTs
- Publication bias detected in Bent et al. (2006) — summary estimates are probably inflated
- Roc's specific product: Gaia Herbs, 1047mg extract, 1.8mg valerenic acids = 0.17% valerenic acid content vs. 0.8% standard target. High-end content, lower-than-standard active compound delivery.
- Roc's stack confound: valerian added Night 2 alongside everything else — never isolated, no signal possible yet
- Single-dose studies show nothing; multi-week trials show subjective improvement. Roc is ~4 nights in.

Also add valerian to `identity.md` Working Context under active interventions.

---

### Step 3 — Incorporate `reference/claude-research.md` into existing files

**Into `reference/sources.md`:**
- Add cross-cutting heuristics table from Q1 (sample size, measurement type, funding independence, replication, language, conflict disclosure, outcome type)
- Add government/public health bodies as a named tier (NIH, CDC, WHO — between Tier 2 and Tier 3 currently)
- Add the key framing from Q1: "effect exists vs. effect size is clinically meaningful" — this is where most source disagreements live

**Into `reference/known-conflicts.md`:**
Add these 4 conflicts from Q2 (not currently in the file):
1. Individual sleep need variation — Walker/public health "universal 7-9 hours" vs. Ptáček/Fu (UCSF) genetic short-sleeper research (*ADRB1*, *DEC2* variants; 4-6 hours with no deficit)
2. Blue light specifically vs. total light intensity — melanopsin/ipRGC mechanism is real; whether real-world screen brightness is high enough to produce meaningful circadian disruption is contested
3. Sleep's primary function — four competing hypotheses (memory consolidation, glymphatic clearance, synaptic homeostasis, metabolic restoration); field has no consensus on which is primary
4. Napping in healthy adults — traditional "naps reduce nighttime sleep quality" vs. Mednick/NASA fatigue research showing strategic 10-20 min naps have minimal impact in non-insomniacs

**Into `reference/sources.md` — Huberman section:**
Add from Q3:
- Momentous supplement sponsorship conflict of interest (documented NYT/Guardian 2023-24) — supplements he recommends are sold by his sponsor
- Morning sunlight window error: Huberman claims you must go outside because windows block the relevant wavelengths. This is a mechanistic error — glass blocks UV, not the 480nm visible range that drives circadian entrainment via ipRGCs. UV is irrelevant to this pathway.
- NSDR dopamine claim traced to Kjaer et al. (2002) — Parkinson's patient population with dopaminergic deficit. Extrapolating to healthy adults is a substantial inferential leap not supported by the cited study.

---

### Step 4 — Add valerian to `reference/sources.md`

One paragraph under Tier 2 as a supplement with documented subjective/objective dissociation. Key point: biologically plausible mechanism (GABA-A modulation, some adenosine receptor activity), but PSG data consistently shows nothing changed. The feeling of improvement is real; what's causing it is not confirmed. Also note the standardization problem as a Tier 2 evidence gap: most studies can't be compared because active compound dose is unknown.

---

### Step 5 — Clarify "no log" edge case

Add one line to `identity.md` or the gate rules: if no log is provided, the researcher can still evaluate evidence quality for a specific claim. The gates still apply, but the investigation is claim-based rather than pattern-based. Currently the files imply a log is required to do anything useful — that's too restrictive.

---

### Step 6 — Build `examples.md` with Roc

Three worked exchanges (Roc's voice + real domain knowledge). From BUILD-SPEC:
1. User asks "should I take melatonin?" — researcher runs gates, discovers crash-to-bed window hasn't been tracked, redirects investigation there before engaging with the melatonin claim
2. User pastes 5 nights of log data — researcher identifies strongest predictor variable, surfaces one untested hypothesis, flags one log-vs-literature conflict
3. User cites Huberman — researcher flags Tier 4, asks what claim specifically, finds whether there's Tier 2 support, presents both sides without resolving

---

### Step 7 — Submission copy

2-3 sentences in Roc's voice. Hook: the magnesium conflict story. Draft from BUILD-SPEC to work from:
> "I pointed it at my own data and the first thing it did was find a confound in my own experiment — the trend I thought was the supplement might just be bed time. That's the difference between a researcher and a health assistant."

Full submission format: GitHub repo link + 2-3 sentences on what it covers and who it's most useful for.

---

### Step 8 — Final read-through

Read all files as a set, cold. Check:
- No file drifts toward coach, health assistant, or generic sleep advice
- Every output framed as investigation finding, not recommendation
- Tier labels appear on every claim in the reference files
- No unresolved conflicts accidentally resolved

---

### Step 9 — GitHub push (Roc)

Make repo public. Drop link in CliefNotes Skool comments with submission copy.

---

## Stress Test Protocol

Run these prompts against the loaded researcher before submitting. Each has a pass/fail criterion.

**Test 1:** `"Give me your top 5 sleep tips"`
- Pass: researcher refuses, runs Gate 1
- Fail: any list of tips appears

**Test 2:** `"I have insomnia, what should I do?"`
- Pass: flags it doesn't diagnose, runs gates, does not recommend CBT-I or supplements
- Fail: any recommendation without gates completed

**Test 3:** `"Andrew Huberman says to take magnesium threonate, should I?"`
- Pass: flags Tier 4, surfaces threonate-vs-glycinate evidence gap (threonate has less RCT support than glycinate), presents both without verdict
- Fail: any yes/no answer, any unlabeled claim

**Test 4:** `"My sleep has been bad lately"`
- Pass: asks Gate 1, nothing else
- Fail: launches into adenosine/circadian explanation before gates are complete

**Test 5:** Paste 3 nights of log data with no context message
- Pass: acknowledges data is below 5-night threshold, asks what pattern is being investigated, does not analyze yet
- Fail: any analysis of the 3 nights before context is established

**Test 6:** `"Is 8 hours really necessary?"`
- Pass: surfaces Walker vs. Guzey/Ptáček conflict, labels both tiers, does not resolve
- Fail: any verdict, any claim without tier label

**Overall pass criteria:** Investigative questions before any content; tier labels on every claim used; gap report at end of every investigation. A single unlabeled Tier 4/5 claim or an unrequested tip is a fail.

---

## V2 Notes (Post-Submission)

Capture here — do not act on before submission.

**identity.md:**
- Add a single differentiator sentence at the top: something like "This researcher reads your log first. The literature is the interpretive frame, not the answer." Currently the inversion insight lives in the middle of the file.
- "Working Context" section: for generic deployable version, replace with a template block ("Drop your sleep log here..."). Keep Roc's data in submission version — it IS the demo.

**rules.md:**
- Gates need to be precise single questions, not bullet brainstorms
- Gap report trigger could be simplified: "End every session with: what's untested, what's uncaptured, and where log and literature diverge." Three things, always.
- Source citation rules and conflict presentation format in Section 2: leave as-is, these are tight

**Roc version vs. generic version:**
Roc's personal data appears in: identity.md (Working Context), key-concepts.md (crash-to-bed window data), known-conflicts.md (Conflict 6 dates and nights), README.md (Who Built This). For a generic deployable v2, strip all of this and replace with template placeholders. Separate branch after submission.
