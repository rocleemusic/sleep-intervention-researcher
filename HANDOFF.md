# HANDOFF — Sleep Intervention Researcher
*CliefNotes Weekly Comp #6: The Researcher*
*Read this first. Then read BUILD-SPEC.md. Then start.*

---

## What This Is

A folder-based AI researcher entry for CliefNotes Comp #6. The full build plan is in `BUILD-SPEC.md` in this directory. Read it before doing anything.

**Deadline: Sunday May 31, 12:00 PM EST.**
**Roc is on the road until ~5:30pm. Your job: build everything that doesn't require his input.**

---

## The Concept

This researcher treats Roc's personal sleep log as Tier 1 data and cross-references it against the sleep science literature — not the other way around. The researcher investigates Roc's crash pattern using science as an interpretive framework, not as a prescription.

Key distinction this comp is judging: **a researcher investigates what's missing, not what's known**. It asks what angle you're working, what you already know, and what sources you've already checked — before saying anything. It surfaces gaps and conflicts. It does NOT summarize.

The "Roc is the experiment" framing: personal observed data (the sleep log) sits at Tier 1 in the credibility hierarchy — above the literature. The literature is used to form hypotheses and weigh evidence, not to hand out tips.

**Do not let any file drift toward coach, health assistant, or generic sleep advice. Every output is an investigation finding, not a recommendation.**

---

## File Structure to Build

```
sleep-intervention-researcher/
  BUILD-SPEC.md         ← already exists — read it
  HANDOFF.md            ← this file
  identity.md           ← BUILD NOW
  rules.md              ← BUILD NOW (gates stubbed — Roc fills in)
  examples.md           ← LEAVE FOR ROC
  reference/
    sources.md          ← BUILD NOW (run research first)
    known-conflicts.md  ← BUILD NOW (run research first)
    key-concepts.md     ← BUILD NOW (run research first)
    log-reading-protocol.md ← BUILD NOW
  README.md             ← BUILD NOW
  .mcp.json             ← already exists
  .claude/settings.json ← already exists
```

---

## Tools Available

**Firecrawl** — installed globally. Use `firecrawl search` and `firecrawl scrape`.
**Tavily** — MCP server configured in `.mcp.json`. Available as MCP tool `tavily` in this session if opened from this project directory.

Use both for the research pass. Firecrawl searches + scrapes. Tavily finds academic and news sources. Together they populate the `reference/` files.

---

## Research Pass — Run Before Writing reference/ Files

### Firecrawl searches (run these):
1. `"Matthew Walker Why We Sleep peer review criticism methodology Alexey Guzey"`
2. `"Andrew Huberman sleep protocol scientific basis criticism evidence"`
3. `"magnesium glycinate sleep quality randomized controlled trial evidence"`
4. `"tart cherry juice melatonin sleep quality peer reviewed study"`
5. `"sleep restriction therapy vs sleep consolidation therapy evidence"`
6. `"evening energy crash postprandial dip circadian adenosine mechanism"`
7. `"Borbély two-process model sleep pressure circadian drive"`
8. `"AASM American Academy Sleep Medicine clinical guidelines recommendations"`
9. `"popular sleep advice claims weak no peer reviewed evidence"`

### Firecrawl scrapes (crawl these specific pages):
1. `https://guzey.com/books/why-we-sleep/` — Guzey's Walker critique (most cited methodological takedown)
2. `https://aasm.org/resources/pdf/healthysleep.pdf` (or AASM sleep recommendations page if PDF fails)
3. Huberman Lab sleep episode show notes — search for it, scrape the page with specific supplement claims

### What to do with the research output:
- Use it to populate `reference/sources.md` with **real examples at each credibility tier** — not made-up examples
- Use the Walker/Huberman content to populate `reference/known-conflicts.md` with documented disagreements and specific disputed claims
- Use the circadian/adenosine/two-process content to populate `reference/key-concepts.md`
- Cite sources with URLs where possible — the comp judges check this

---

## Roc's Sleep Pattern (for identity.md and log-reading-protocol.md context)

Read `P:\GitHub\RL_MAP\RL_MAP\6-month-orchestrator\sleep-log.md` for the actual pattern.

Summary:
- Evening crash: ~8–9pm most nights (body crashes ~2 hours after work ends)
- Crash-to-bed window: 3–5 hours (crashes early, goes to bed much later)
- Total sleep: improving — 5h40min → 6h → 6h45min over recent nights
- Mid-night wake: occasionally around 5am
- Key variable identified: earlier bed time → longer total sleep
- Phase 1 active: magnesium glycinate + tart cherry juice 30 min before bed
- Phase 2 active: walk after dinner (7:30pm) — testing postprandial dip intervention

This is the specific pattern the researcher is scoped to. Not generic insomnia. Not sleep onset difficulty. The specific problem: **early crash, large crash-to-bed gap, improving but inconsistent totals.**

---

## What to Build (Your Job)

### identity.md
Who the researcher is, domain scope, what it covers, what it doesn't. Key points:
- Investigates sleep intervention evidence for people with evening crash + disrupted sleep architecture
- Treats user's personal sleep log as Tier 1 data
- Cross-references against peer-reviewed literature as interpretive framework
- Does NOT: diagnose, prescribe clinical treatment, act as coach, summarize generic sleep hygiene
- Most useful when user has 5+ nights of logged data

### rules.md
Three behavior sections. Write these in full:
1. **Source citation rules** — every claim gets a tier label before use; never synthesize a Tier 4/5 claim without flagging the tier; conflict between tiers = present both, do not resolve
2. **Gap reporting rules** — always end with what hasn't been tested; surface what the log hasn't captured; flag when log data contradicts literature prediction
3. **Pre-research gates** — write the section header and structure, but leave the actual gate questions as `[STUB — Roc to fill from road thinking]`. The gates are the most important part of rules.md and must come from Roc's lived experience of the problem.

### reference/sources.md
Build from research output. Must have:
- Tier system (Tier 1 personal data through Tier 5 supplement marketing)
- Real named examples at each tier with brief credibility notes
- Specific notes on Walker and Huberman (named sources at Tier 4 with specific methodology caveats)
- At least one Tier 2 example with a real study citation

### reference/known-conflicts.md
Build from research output. Each conflict entry:
- Names both sides of the disagreement
- Labels each side's evidence tier
- Does NOT resolve the conflict — presents both
- Minimum 5 conflicts documented

### reference/key-concepts.md
Backbone definitions the researcher uses without hallucinating:
- Sleep architecture (NREM stages, REM, 90-min cycles)
- Adenosine system (buildup, clearance, caffeine mechanism)
- Circadian rhythm (SCN, zeitgebers, phase advance/delay)
- Two-process model — Borbély (sleep pressure + circadian drive)
- Postprandial dip (post-meal energy drop, timing, mechanism)
- Crash-to-bed window (defined term used in Roc's log)

### reference/log-reading-protocol.md
How to interpret personal sleep log data. Key points:
- What fields matter: crash time, bed time, wake time, total, feeling, mid-wake
- Derived variables: crash-to-bed window, total sleep trend, feeling vs. total correlation
- Weighting N=1 data: observed > predicted; personal pattern > population average
- What the log CAN tell you (behavioral patterns) vs. CANNOT (mechanism)
- When log data conflicts with literature: that gap IS the investigation
- Minimum data for useful investigation: 5 nights with full fields

### README.md
Cold-start instructions. How to use it with no context:
1. Drop folder into a Claude project
2. Upload your sleep log (any format)
3. Tell the researcher what pattern you're investigating
4. Expect: questions first, investigation second, gaps named throughout
5. What it won't do: give you a list of tips, diagnose anything, tell you what to do

Include one worked example of a first message and what the researcher should ask in response (investigative, not prescriptive).

---

## What to Leave for Roc

- **`examples.md`** — 2-3 worked exchanges. Needs Roc's voice and real domain knowledge. Do not draft this.
- **Pre-research gate questions in `rules.md`** — the specific questions the researcher asks before engaging. These must reflect lived experience. Mark as `[STUB]`.
- **Submission copy** — the 2-3 sentences for the CliefNotes comment. Do not draft this.
- **GitHub push** — Roc does this.
- **Final review** — Roc reads all files before submission.

---

## When Roc Returns (~5:30pm)

Tell him:
1. What files are done
2. What the stubs in rules.md are waiting on (the gate questions)
3. Any conflicts found in the research that are worth his attention
4. What examples.md needs from him to be written

Then go straight into building examples.md together.

---

## Definition of Done (for your session)

- [ ] Research pass complete (Firecrawl + Tavily queries run)
- [ ] `reference/sources.md` — real examples at each tier, URLs where possible
- [ ] `reference/known-conflicts.md` — 5+ documented conflicts, unresolved
- [ ] `reference/key-concepts.md` — 6 core concepts defined
- [ ] `reference/log-reading-protocol.md` — complete
- [ ] `identity.md` — complete
- [ ] `rules.md` — source citation + gap reporting complete; gates stubbed
- [ ] `README.md` — complete with worked first-message example
- [ ] `examples.md` — NOT built (Roc's job)
- [ ] Gate questions in `rules.md` — NOT filled (Roc's job)
