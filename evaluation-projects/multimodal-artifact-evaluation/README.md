# Multimodal Artifact Evaluation

## Overview

This project demonstrates a structured approach to evaluating AI-generated multimodal artifacts, including interactive interfaces, games, documents, visual outputs, and other artifact-based responses.

The evaluation process focuses on:

- Prompt and input understanding
- Artifact loading and usability
- Broken or blank interface detection
- Interactive behavior
- Independent rubric evaluation
- Rubric quality and modification
- Evidence-based judgment
- Rejection decisions
- Evaluation quality assurance

The project is based on a synthetic evaluation dataset and does not contain proprietary production data.

---

## Evaluation Objective

The goal is to evaluate whether an AI-generated artifact satisfies the task requirements and whether the evaluation itself is performed consistently and correctly.

The evaluator should separate:

1. Artifact functionality
2. Artifact quality
3. Rubric applicability
4. Evaluation evidence
5. Final QA

A visually unattractive or incomplete artifact should not automatically be rejected.

A sample should only be rejected when the artifact is genuinely broken or blank according to the defined loading and rejection rules.

---

## Evaluation Scope

This project covers:

- Text-based artifacts
- Visual artifacts
- Interactive interfaces
- Forms
- Navigation
- Games
- Multimodal outputs
- Artifact-based agent responses

The evaluation framework can be adapted to different artifact types while keeping the same core evaluation logic.

---

## Evaluation Workflow

### Step 1 — Read the Task

Review:

- User prompt
- Input materials
- Task requirements
- Expected output
- Evaluation rubric

Do not evaluate the artifact before understanding what the task requires.

---

### Step 2 — Open Both Outputs

Open both Response A and Response B.

Both outputs must be opened before completing the evaluation.

The evaluator should not judge one response only because the other response has not yet been inspected.

---

### Step 3 — Check Loading State

After opening an artifact, allow up to 30 seconds for loading.

A loading artifact may contain:

- Spinner
- Progressive rendering
- Partial content
- Delayed interface initialization
- Temporary loading state

Slow loading alone is not a rejection reason.

---

### Step 4 — Detect Broken or Blank Outputs

After the loading period, determine whether the artifact is actually usable.

Examples of broken or blank states:

- Completely blank page
- Black or empty interface
- Error screen
- Unusable tiny fragment
- Persistent loading after the allowed period
- Interface that fails to render the artifact

If one or both outputs are genuinely broken or blank, reject the sample.

Recommended rejection reason:

> One or both outputs have a broken/blank interface

---

## Loading vs Broken

| Situation | Evaluation Action |
|---|---|
| Spinner appears temporarily | Continue waiting |
| Content progressively appears | Continue evaluation |
| Slow rendering but usable | Continue evaluation |
| Poor visual design | Score normally |
| Missing requirement | Score normally |
| One button does not work | Score normally |
| Partial interaction failure | Score normally |
| Completely blank interface | Reject |
| Error interface | Reject |
| Infinite loading after 30 seconds | Reject |

The key distinction is:

**Poor quality is not the same as a broken artifact.**

---

## Step 5 — Test Interactions

For interactive artifacts, test the available interaction paths.

Examples:

- Buttons
- Menus
- Forms
- Links
- Scrolling
- Arrows
- WASD
- Space
- Enter
- Mouse interaction
- Cursor lock
- Escape to exit cursor lock

A failed interaction should normally be treated as a quality issue rather than an automatic rejection.

---

## Game Evaluation

For games or game-like artifacts:

1. Click the artifact to establish focus.
2. Test available controls.
3. Test movement.
4. Test buttons and menus.
5. Test scrolling or navigation when applicable.
6. Test Space or Enter when relevant.
7. Test Escape to exit cursor lock when applicable.
8. Determine whether the artifact remains usable.

A game with poor controls should normally remain eligible for scoring.

Only a genuinely broken or blank artifact should be rejected.

---

## Step 6 — Evaluate the Rubric Independently

Each rubric criterion should be evaluated independently for Response A and Response B.

Possible results:

- Good
- Bad
- Not Evaluated

Both outputs can receive the same result.

For example:

| Criterion | Response A | Response B |
|---|---|---|
| Visual consistency | Good | Good |
| Requirement coverage | Bad | Good |
| Interaction | Good | Bad |

The evaluator should not force a difference between the two outputs.

---

## Step 7 — Review the Rubric

The rubric itself may contain problems.

Possible actions:

### Remove

Use when:

- The criterion cannot be evaluated.
- The criterion is clearly not applicable.
- The artifact does not contain the required component.

### Clarify

Use when:

- The criterion is relevant.
- The wording is ambiguous.
- A small wording change makes it objectively evaluable.

### Correct

Use when:

- The criterion conflicts with the prompt.
- The criterion references a nonexistent document.
- The criterion contains an incorrect requirement.

Rubric modifications must be applied neutrally.

Do not modify a rubric to make one response look better.

---

## Step 8 — Record Evidence

Every important judgment should be supported by observable evidence.

Good evidence describes:

- What was observed
- Where it occurred
- What requirement it affects
- Why the observation supports the judgment

Avoid vague statements such as:

> Response A is better.

Prefer:

> Response A loads successfully and exposes all required navigation controls, while Response B leaves the primary navigation menu non-functional.

---

## Step 9 — Complete Overall Evaluation

After individual criteria are evaluated, complete the overall evaluation.

The overall assessment should reflect the evidence gathered from:

- Requirement coverage
- Artifact quality
- Functionality
- Interaction
- Usability
- Rubric results

Do not allow a single minor issue to dominate the entire evaluation unless the rubric explicitly makes that issue critical.

---

## Rejection Decision Tree

```text
Open artifact
      |
      v
Does it load?
      |
   +--+--+
   |     |
  No    Yes
   |     |
Wait     v
up to   Test
30 sec  artifact
   |     |
   v     v
Still   Usable?
broken?   |
   |     |
  Yes   +--+--+
   |    |     |
Reject Yes    No
        |      |
      Score   Score
      normally normally
