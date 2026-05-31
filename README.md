# Sleep Intervention Researcher
*A folder-based AI researcher for people with disrupted sleep patterns who keep getting generic advice.*

---

## What This Is

This researcher treats your personal sleep log as the primary data source and cross-references it against the sleep science literature — not the other way around. Generic sleep advice fails because it applies population averages to specific individuals. This one can't be generic: your log is the experiment.

**The angle:** Investigative, not prescriptive. The researcher asks what's missing before it says anything. It surfaces gaps and conflicts. It does not summarize.

---

## How to Use It (Cold Start)

### 1. Drop this folder into a Claude project

Add the entire `sleep-intervention-researcher/` folder as project context. Everything in `reference/` is loaded automatically.

### 2. Upload your sleep log

Any format works — plain text, markdown, a table, a photo of a notebook.

**No log yet?** Use `reference/log-template.md` — it has the full field list with a blank entry you can copy and notes on what each field captures.

**Want to test first?** Use `reference/demo-sleep-log.md` — 7 nights of fictional data with a mid-log intervention. Load it and ask: *"I started magnesium on Night 4 and my sleep is improving. Is it working?"*

The more nights, the better. Five nights minimum for pattern investigation.

### 3. Tell the researcher what pattern you're investigating

Not "I want better sleep." That's too broad. Name the specific thing:
- "I crash at 8pm every night and don't go to bed until 2am"
- "I keep waking up at 4-5am and can't get back to sleep"
- "I tried magnesium and I think it's working but I don't know"
- "Huberman said to take apigenin — I want to know if there's evidence for that"

### 4. Expect: questions first, investigation second

The researcher will run through a set of pre-research gates before engaging with your pattern. These are not bureaucratic — they prevent investigations that don't fit the actual problem.

Expect to answer:
- What exactly is the pattern (specific timing, specific symptom)
- What you've already tried and what changed
- What source or claim is informing your current approach
- What decision you're trying to make

After the gates: investigation. The researcher will cross-reference your log against relevant concepts in the `reference/` files, flag evidence tiers, name conflicts, and end every session with what hasn't been tested.

### 5. What it won't do

- Give you a list of sleep tips
- Tell you what to do
- Diagnose anything
- Resolve source conflicts into a verdict
- Repeat information from the literature without labeling its evidence tier

---

## Worked Example — First Message and Response

**User's first message:**

> "I've been taking magnesium glycinate for 4 nights and my sleep is going up. 5h40, 6h, 6h45 over the last three nights. Is it working?"

**What the researcher asks (not what it answers):**

> Before we can say whether the magnesium is the cause: I have a few questions I need to work through.
>
> First: what exactly changed when you started taking it? Not just the magnesium — what else was different on those nights? Bed time, what you did before bed, stress level, whether you woke up mid-night?
>
> I'm asking because your log shows improving totals, but "improving" can come from several places. The magnesium is one candidate. Bed time is another — if you went to bed earlier on the better nights, that's a more likely explanation than the supplement, because the evidence for magnesium's effect size in healthy adults is modest at best.
>
> What did your bed times look like across those four nights?

*Note what happened: The researcher didn't answer the question. It asked the question that determines whether the question can be answered. It flagged the confound (bed time) before the user even knew it was a confound. It cited the evidence tier implication without making it a lecture.*

*For full investigation outputs — tier-labeled mechanism breakdown, fork analysis, and gap reports — see `examples.md`.*

---

## File Map

```
sleep-intervention-researcher/
  identity.md               ← who the researcher is and what it investigates
  rules.md                  ← investigative behavior: gates, citation rules, gap reporting
  examples.md               ← worked exchanges showing investigative vs. summarizing behavior
  reference/
    sources.md              ← credibility tier system, sourced from Tier 2 meta-analyses and Tier 3 AASM clinical guidelines
    known-conflicts.md      ← documented disagreements in sleep science, unresolved
    key-concepts.md         ← sleep architecture, adenosine, circadian, two-process model
    log-reading-protocol.md ← how to read and weight personal sleep log data
    log-template.md         ← blank entry schema for users without a log
    demo-sleep-log.md       ← 7 nights of fictional data for testing the researcher
  README.md                 ← this file
```

