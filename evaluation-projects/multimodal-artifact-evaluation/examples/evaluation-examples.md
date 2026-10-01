# Multimodal Artifact Evaluation Examples

## Purpose

This file provides practical examples of how an evaluator should apply the multimodal artifact evaluation workflow.

The examples focus on:

- Loading vs broken states
- Interaction testing
- Game controls
- Independent rubric evaluation
- Rubric modification
- Evidence-based judgment
- Rejection decisions
- Evaluation QA

---

## Example 1 — Slow Loading

### Observation

Response A takes approximately 20 seconds to render.

Response B renders immediately.

### Decision

Do not reject Response A.

### Reason

The artifact becomes usable within the allowed loading period.

---

## Example 2 — Blank After 30 Seconds

### Observation

Response A remains completely blank after the allowed loading period.

Response B renders normally.

### Decision

Reject the sample.

### Rejection Reason

> One or both outputs have a broken/blank interface.

---

## Example 3 — Poor Visual Design

### Observation

Response A is cluttered and visually inconsistent.

The interface still loads and can be used.

### Decision

Continue evaluation.

### Reason

Poor visual quality should affect the evaluation result, not automatically trigger rejection.

---

## Example 4 — Broken Button

### Observation

The main interface loads correctly, but one secondary button does not respond.

### Decision

Continue evaluation.

### Reason

A partial interaction failure does not automatically make the entire artifact broken.

The interaction problem should be recorded as evidence.

---

## Example 5 — Game Controls

### Observation

A game loads successfully.

The evaluator tests:

- Arrow keys
- WASD
- Space
- Enter
- Mouse

Some controls work while others do not.

### Decision

Continue evaluation.

### Reason

The game is still observable and evaluable.

Control problems should affect the relevant quality criteria.

---

## Example 6 — Cursor Lock

### Observation

The game captures the mouse cursor.

The evaluator presses Escape.

### Decision

Continue evaluation if the cursor is released successfully.

### Reason

Cursor lock should be tested when relevant to the game experience.

---

## Example 7 — Both Outputs Good

### Observation

Response A satisfies the criterion.

Response B also satisfies the criterion.

### Correct Evaluation

```text
Response A: Good
Response B: Good
