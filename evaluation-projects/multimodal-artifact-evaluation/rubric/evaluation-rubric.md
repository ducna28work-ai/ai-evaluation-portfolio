# Multimodal Artifact Evaluation Rubric

## 1. Task Understanding

Evaluate whether the artifact addresses the requirements described in the prompt and input materials.

### Good

The artifact substantially addresses the stated requirements.

### Bad

The artifact misses important requirements or does not adequately address the task.

---

## 2. Artifact Availability

Evaluate whether the artifact becomes usable after the expected loading period.

### Good

The artifact loads and provides a usable interface.

### Bad

The artifact remains fundamentally unavailable for evaluation.

---

## 3. Interactive Functionality

Evaluate relevant interactions based on the artifact type.

Possible checks include:

- Buttons
- Menus
- Forms
- Navigation
- Scrolling
- Mouse controls
- Keyboard controls
- Game controls
- Focus behavior

### Good

Relevant interactions work sufficiently for the requested task.

### Bad

Important interactions fail or prevent meaningful use.

---

## 4. Rubric Compliance

Evaluate each task-specific rubric criterion independently.

Each response should receive its own:

- Good
- Bad

rating.

The evaluator should not convert individual rubric criteria directly into an A/B winner selection.

---

## 5. Overall Preference

After evaluating the rubric independently, compare the two artifacts overall.

The overall comparison should consider:

- Task fulfillment
- Rubric performance
- Usability
- Interaction quality
- Overall artifact quality

---

## 6. Loading vs Broken

### Loading

Indicators include:

- Spinner
- Progressive rendering
- Partial interface appearing
- Continued loading activity

Allow the artifact sufficient time to render before making a broken-interface judgment.

### Broken or Blank

Examples include:

- Persistent blank screen
- Persistent black screen
- Blocking error
- Unusable partial interface
- Indefinite loading

---

## 7. Rejection

Reject only when the artifact is fundamentally unavailable for evaluation.

Do not reject solely because:

- The artifact looks poor.
- The output is incomplete.
- A requirement is missing.
- Some interactions fail.
- Game mechanics are broken.
- The output has low quality.

These issues should normally be reflected in the rubric evaluation.

---

## 8. Rubric Editing

### Remove

Use when a criterion cannot be evaluated from the available materials or is clearly not applicable.

### Clarify

Use when minor wording changes can make the criterion objectively evaluable while preserving the original intent.

### Correct

Use when the criterion directly conflicts with the prompt or references nonexistent material.

Rubric modifications must:

- Preserve original intent.
- Apply equally to both responses.
- Be supported by task evidence.
- Avoid favoring either response.

---

## 9. QA Levels

### 5 — Exceptional

- Both artifacts are fully inspected.
- Loading and broken states are distinguished correctly.
- Relevant interactions are tested.
- Rubric criteria are evaluated independently.
- Rejection is used correctly.
- Overall judgment is evidence-based.
- Rubric modifications are justified and unbiased.

### 4 — Strong

- Both artifacts are evaluated accurately.
- Required interactions are tested.
- Minor depth or evidence gaps may remain.

### 3 — Acceptable

- Overall evaluation is generally reasonable.
- Interaction testing may be limited.
- Some evidence or rubric reasoning may be incomplete.

### 2 — Weak

- Artifact inspection is incomplete.
- Loading and broken states may be confused.
- Rubric modifications lack sufficient justification.
- Important interactions may be missed.

### 1 — Unacceptable

- Both artifacts are not properly inspected.
- An output is rejected simply because it is poor quality or slow to load.
- Rubric changes are made to favor a response.
- Interactive outputs are not meaningfully tested.
