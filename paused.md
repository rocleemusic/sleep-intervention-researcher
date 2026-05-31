# Paused — Sleep Intervention Researcher v1
*Status as of May 31, 2026. Do not execute — reference only.*

---

## What's Done

- `reference/sources.md` — tier system, real named examples, Walker/Huberman caveats; cross-cutting credibility heuristics table added; "effect exists vs. effect size" framing added; government/public health bodies (Tier 2/3) section added; valerian entry (subjective/objective dissociation) added; Huberman section expanded with Momentous sponsorship conflict, sunlight window mechanism error, NSDR dopamine claim extrapolation
- `reference/known-conflicts.md` — 11 conflicts documented, all unresolved (added: individual sleep need variation, blue light vs. total light intensity, sleep's primary function, napping in healthy adults, valerian subjective/objective dissociation)
- `reference/key-concepts.md` — 6 core concepts, crash-to-bed window populated with Roc's data
- `reference/log-reading-protocol.md` — complete including first-contact gate prerequisite; tiered data minimums added (5–7 nights for pattern, 14+ for intervention evaluation with isolated baseline, 30+ for trend detection)
- `identity.md` — complete; valerian added to Working Context active interventions; no-log user path updated in "Not optimized for"
- `rules.md` — all four gates filled (questions, example prompts, "what this catches" notes); first-contact hard rule added ("ask Gate 1 before engaging with anything"); no-log protocol section added; substances/medications reactive gate rule added; standing gap report item for substances/medications added
- `README.md` — complete with worked first-message example
- `BUILD-SPEC.md` — submission notes section added (magnesium conflict story + log schema changes)
- `sleep-log.md` — alarm field added to Morning block schema; onset latency historical note added
- `reference/claude-research.md` and `reference/valerian-root.md` — moved out of reference/ (content fully incorporated into structured files)

---

## To Finish v1 (In Order)

### Step 6 — Write `examples.md`

Three worked exchanges exist from Roc's test runs — researcher behaved correctly in all three. Write them into `examples.md`.

Exchange 1: "should i take magnesium" — researcher ran all 4 gates, tiered the YouTube source, produced full investigation + gap report with substances prompt.

Exchange 2: "here is my sleep log" — researcher ran gates (Gate 1 answered from log itself), did fork analysis (Fork A: close gap from bed side; Fork B: push crash later), gap report flagged caffeine and dinner timing as missing variables.

Exchange 3: "I have a problem of crashing after dinner" — researcher ran all 4 gates, broke down three concurrent crash mechanisms (adenosine, postprandial, circadian), flagged walk timing distinction (after dinner vs. after work), gap report with melatonin timing as uncontrolled variable.

**First move when we resume:** Format the three test exchanges and write into `examples.md`.

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
- Gap report trigger could be simplified: "End every session with: what's untested, what's uncaptured, and where log and literature diverge." Three things, always.
- Source citation rules and conflict presentation format in Section 2: leave as-is, these are tight

**Roc version vs. generic version:**
Roc's personal data appears in: identity.md (Working Context), key-concepts.md (crash-to-bed window data), known-conflicts.md (Conflict 6 dates and nights), README.md (Who Built This). For a generic deployable v2, strip all of this and replace with template placeholders. Separate branch after submission.
