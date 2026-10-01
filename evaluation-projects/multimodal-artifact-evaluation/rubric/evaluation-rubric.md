# Multimodal Artifact Evaluation — QA Rubric

## Purpose

This rubric evaluates the quality of the evaluator's work rather than the quality of the AI artifact itself.

---

## 5 — Exceptional

The evaluator:

- Fully understands the prompt and input materials.
- Opens and inspects both responses.
- Correctly distinguishes loading from broken/blank states.
- Applies the 30-second loading rule correctly.
- Tests relevant interactions thoroughly.
- Tests game controls when applicable.
- Evaluates rubric criteria independently.
- Makes only justified rubric modifications.
- Keeps rubric modifications neutral.
- Provides specific observable evidence.
- Uses rejection only when appropriate.
- Maintains consistent reasoning throughout the evaluation.

---

## 4 — Strong

The evaluator completes the major evaluation steps correctly.

Minor omissions may exist, but they do not materially affect the final evaluation.

---

## 3 — Acceptable

The evaluator completes the core workflow but has noticeable weaknesses.

Examples:

- Limited interaction testing
- Weak evidence
- Minor inconsistency
- Incomplete rubric explanation

The final decision remains generally usable.

---

## 2 — Weak

The evaluator misses important parts of the workflow.

Examples:

- Incomplete artifact inspection
- Weak loading assessment
- Limited interaction testing
- Poor evidence
- Inconsistent rubric application

The evaluation requires substantial QA review.

---

## 1 — Unacceptable

The evaluator:

- Does not inspect both outputs.
- Rejects slow loading without applying the loading rule.
- Rejects low-quality outputs that are still usable.
- Fails to reject genuinely broken/blank outputs.
- Evaluates only by comparison.
- Modifies the rubric to favor one response.
- Does not test relevant interactions.
- Provides unsupported judgments.

---

## QA Error Taxonomy

### E1 — Incomplete Inspection

One or both responses were not properly inspected.

### E2 — Loading Error

The evaluator incorrectly treats slow loading as broken.

### E3 — Rejection Error

The evaluator rejects a usable artifact or fails to reject a genuinely broken artifact.

### E4 — Interaction Error

Relevant controls were not tested.

### E5 — Rubric Bias

The evaluator modifies criteria in a way that favors one response.

### E6 — Rubric Misapplication

A criterion is applied incorrectly or inconsistently.

### E7 — Evidence Failure

The evaluator provides conclusions without observable evidence.

### E8 — Comparison Bias

The evaluator judges a response primarily by whether it is better or worse than the other response rather than against the criterion.

---

## Final QA Gate

Before accepting an evaluation, confirm:

```text
[ ] Prompt understood
[ ] Input materials reviewed
[ ] Response A opened
[ ] Response B opened
[ ] Loading state checked
[ ] Broken/blank decision correct
[ ] Relevant interactions tested
[ ] Game controls tested when applicable
[ ] Rubric evaluated independently
[ ] Rubric changes justified
[ ] Rubric changes neutral
[ ] Evidence recorded
[ ] Overall evaluation completed
[ ] Rejection decision justified
[ ] Final QA completed
