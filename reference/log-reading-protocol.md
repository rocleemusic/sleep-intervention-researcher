# Log Reading Protocol
*How to interpret and weight personal sleep log data. Read before any investigation.*

---

## What Fields Matter

A useful sleep log entry contains at minimum these fields. Any field that's missing reduces the investigation value of that night's data.

| Field | What it captures | Why it matters |
|-------|-----------------|----------------|
| **Crash time** | When the body went offline involuntarily | The primary indicator of sleep pressure and circadian phase |
| **Bed time** | When the person actually got into bed | Defines the crash-to-bed window |
| **Wake time** | When sleep ended | Determines total possible sleep window |
| **Total sleep** | Actual duration (not window) | The outcome variable — what everything else is trying to explain |
| **Feeling rating** | Subjective quality on a consistent scale | Captures what total alone misses (e.g., 6h interrupted vs. 6h solid) |
| **Mid-night wakes** | Any wake-ups, approximate time | Distinguishes sleep continuity issues from total issues |
| **Phase notes** | What interventions were active | Allows correlation across multiple nights |
| **Work end time** | When the work day ended | Sets the clock on the waking window — hours awake before crash |

**Secondary fields (useful when present):**
- Walk/exercise timing
- Meal timing (especially last meal)
- Caffeine cutoff time
- Subjective stress level

---

## Derived Variables to Calculate

Don't just read the fields — derive these before starting any investigation.

**Crash-to-bed window:** `bed time − crash time`
The gap between when the body wanted sleep and when sleep was allowed. This is often the most useful single variable in the log.

**Total sleep trend:** Calculate rolling average over the last 5 nights. One night's total is noise. Five nights of totals with context starts to show signal.

**Feeling vs. total correlation:** Does higher total sleep produce better feeling scores? If yes: total is the limiting factor. If no: something else is disrupting quality (mid-wakes, sleep stage disruption, timing mismatch).

**Hours awake before crash:** `crash time − wake time`
Maps onto predicted adenosine load. If consistently 11-13 hours, the crash is meeting biological expectation. If 8-9 hours, earlier crash may indicate unusual fatigue, illness, or adenosine system variability.

**Intervention nights vs. baseline:** Tag nights where specific Phase 1 or Phase 2 interventions were active. You cannot assess intervention effect without comparing to nights where it was absent.

---

## Weighting N=1 Data

**The core principle:** Observed > predicted. A pattern that appears consistently in Roc's log over 5+ nights takes precedence over what population studies predict for the average person.

**Why:** Population studies report averages across thousands of people with different genetics, schedules, health status, and baseline sleep patterns. The average is not the individual. An intervention that works for 60% of study participants may or may not work for this person.

**Threshold for confidence:**
- 1-2 nights: anecdote. Interesting, not reliable.
- 3-4 nights: suggestive pattern. Worth noting, not worth acting on alone.
- 5-7 nights: reliable enough to form an investigation hypothesis.
- 10+ nights with consistent conditions: strong enough to draw tentative conclusions about this individual.

**The N=1 limitation:** The log can show that X correlates with Y for this person. It cannot prove X causes Y. Causation requires either controlled variation (one variable changed, everything else held constant) or convergent evidence from the literature.

**How to hold both:** "The log shows that on nights when bed time is before 2am, total sleep is over 6 hours. This is consistent with the literature prediction that earlier bed time in a high-sleep-pressure state produces longer totals. The mechanism is Process S + Process C alignment. Roc's data and the framework agree."

---

## What the Log CAN and CANNOT Tell You

### CAN tell you:
- Whether a behavioral pattern correlates with a sleep outcome
- Whether an intervention is associated with a change in outcome across multiple nights
- What the crash-to-bed window is and whether it's changing
- Whether total sleep is trending in a direction
- Whether mid-night wakes cluster at a specific time
- Whether subjective feeling tracks with objective total

### CANNOT tell you:
- **Mechanism** — the log shows what happens, not why. "I crash at 8pm" is observed. "I crash because of adenosine" is a hypothesis requiring Tier 2 support to weigh.
- **Sleep stage distribution** — without polysomnography, you don't know how much N3 vs. REM occurred. Total sleep ≠ quality sleep.
- **Whether an intervention caused an improvement** — without controlled comparison (other variables held constant), improvement may be due to anything.
- **Individual physiology** — the log captures behavior, not biology. Circadian phase, adenosine sensitivity, cortisol profile are not visible.

---

## When Log Data Conflicts with Literature

**This is the investigation.** When the log shows something the literature does NOT predict, that gap is not an error in the log or a reason to dismiss the log. It is the most valuable signal in the dataset.

**Example of a conflict:** The literature predicts that a postprandial dip after dinner should cause a crash 1-2 hours post-meal. But on May 28, Roc skipped the walk and had a plugin session for 1.5 hours instead — and the crash was at 9:10pm, which is later than on nights with the walk (8-9pm range). If the walk is supposed to delay the crash, the data shows the opposite on this one night. That's a gap worth naming.

**How to handle log-vs-literature conflicts:**
1. Name the conflict explicitly: "The log shows X. The literature predicts Y. This is a discrepancy."
2. List candidate explanations without picking one: "This could be because [A], [B], or [C], or because the literature doesn't apply to this pattern."
3. Flag what data would resolve it: "To investigate, we'd need [N more nights with this variable isolated]."
4. Do not resolve: "The log wins when there's enough nights of consistent data. Right now there's not enough to override the literature prediction."

---

## Minimum Data for Useful Investigation

**5 nights with full fields** before drawing any conclusions about pattern.

With fewer nights:
- Use for orientation only — "here's what the data shows so far"
- Flag that conclusions are preliminary
- Ask for more data before making recommendations about protocol changes

**Why 5 nights:** Any single night can be anomalous. Any two nights can suggest a trend that reverses on night three. Five nights with consistent conditions starts to separate signal from noise.

**Exception:** Acute, dramatic changes (e.g., adding a new supplement and getting 9 hours on night 1 after averaging 5h) are worth flagging immediately as a hypothesis — but not a conclusion.

---

## First Contact Protocol

When a user first provides log data:

1. **Count the nights.** Is there enough data for investigation, or orientation only?
2. **Check for full fields.** Which fields are missing? Name them.
3. **Calculate the derived variables.** Crash-to-bed window. Total sleep trend. Feeling vs. total correlation.
4. **Identify the strongest predictor.** What single variable has the clearest correlation with total sleep or feeling rating?
5. **Name one untested hypothesis.** What's the most plausible thing the log suggests but hasn't been tested yet?
6. **Name one gap.** What field or condition would, if tracked, most improve the investigation quality?
