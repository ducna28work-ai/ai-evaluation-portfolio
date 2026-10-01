# TTS Audio Evaluation — QA Rubric

## Purpose

This rubric evaluates the quality of the evaluator's work.

It does not evaluate the TTS system itself.

---

## 5 — Exceptional

The evaluator:

- Reads the transcript before listening.
- Listens to both complete clips.
- Uses appropriate listening conditions.
- Separates the three primary evaluation dimensions correctly.
- Uses audible evidence.
- Avoids speaker identity judgments.
- Avoids target-speaker similarity judgments.
- Handles close calls appropriately.
- Applies rejection rules correctly.
- Selects exactly one Overall Preference.
- Selects exactly one Dominant Factor.
- Ensures the Dominant Factor matches one of the primary dimensions.
- Maintains consistent reasoning.

---

## 4 — Strong

The evaluator completes the major evaluation steps correctly.

Minor omissions may exist but do not materially affect the final result.

---

## 3 — Acceptable

The evaluator completes the core process but has noticeable weaknesses.

Examples:

- Limited evidence
- Incomplete explanation
- Minor dimension confusion
- Limited replay for a close call

The evaluation remains generally usable.

---

## 2 — Weak

The evaluator makes important process mistakes.

Examples:

- Does not fully listen to both clips
- Confuses Naturalness with Audio Quality
- Provides weak evidence
- Applies rejection inconsistently
- Does not properly check the Dominant Factor

The evaluation requires substantial QA review.

---

## 1 — Unacceptable

The evaluator:

- Does not listen to both outputs.
- Judges from the transcript alone.
- Evaluates speaker identity.
- Evaluates target-speaker similarity.
- Confuses technical quality with pronunciation.
- Confuses pronunciation with naturalness.
- Fails to provide evidence.
- Uses invalid rejection reasoning.
- Does not select a valid Dominant Factor.
- Selects multiple overall preferences.

---

# Error Taxonomy

## E1 — Incomplete Listening

One or both audio clips were not fully evaluated.

## E2 — Audio Quality Confusion

Technical artifacts are incorrectly evaluated as pronunciation or naturalness.

## E3 — Pronunciation Confusion

Transcript accuracy problems are incorrectly evaluated as naturalness.

## E4 — Naturalness Confusion

Pacing, pauses, emphasis, or intonation are incorrectly evaluated as technical audio problems.

## E5 — Speaker Identity Bias

The evaluator judges whether the speaker resembles a specific person.

## E6 — Target Voice Bias

The evaluator judges similarity to a hidden or imagined target speaker.

## E7 — Rejection Error

The evaluator rejects a sample without meeting the rejection conditions.

## E8 — Evidence Failure

The judgment is not supported by an observable audio-based reason.

## E9 — Dominant Factor Error

The selected Dominant Factor does not explain the Overall Preference.

## E10 — Multiple Preference Error

The evaluator fails to select exactly one overall preferred response.

---

# Final QA Gate

```text
[ ] Transcript reviewed
[ ] A fully listened to
[ ] B fully listened to
[ ] Audio quality evaluated
[ ] Pronunciation evaluated
[ ] Naturalness evaluated
[ ] Overall Preference selected
[ ] Exactly one Dominant Factor selected
[ ] Dominant Factor is valid
[ ] Speaker identity excluded
[ ] Target-speaker similarity excluded
[ ] Close call replay performed when necessary
[ ] Evidence supports the judgment
[ ] Rejection decision is valid
[ ] Final evaluation is internally consistent
