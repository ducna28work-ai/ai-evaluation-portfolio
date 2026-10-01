# Multimodal Evaluation Dataset

## Purpose

This dataset contains synthetic evaluation records designed to demonstrate multimodal artifact evaluation and QA.

The dataset covers:

- Artifact loading
- Broken and blank interfaces
- Interactive behavior
- Game controls
- Independent rubric evaluation
- Rubric modification
- Evidence-based decisions
- Rejection handling
- Evaluation QA

---

## Dataset Schema

| Field | Description |
|---|---|
| `case_id` | Unique evaluation case |
| `scenario` | Main evaluation scenario |
| `task_type` | Artifact or interaction type |
| `response_a_observation` | Observation for Response A |
| `response_b_observation` | Observation for Response B |
| `rubric_result_a` | Rubric result for Response A |
| `rubric_result_b` | Rubric result for Response B |
| `overall_result` | Overall evaluation outcome |
| `special_action` | Rejection or rubric action |
| `evidence` | Observable evidence |
| `qa_status` | QA review status |

---

## Rubric Result Values

Allowed values:

- `Good`
- `Bad`
- `Not Evaluated`

`Not Evaluated` is used when a criterion cannot reasonably be evaluated, such as when the entire artifact is rejected because it is broken or blank.

---

## Special Actions

Possible values include:

- `None`
- `Reject`
- `Remove`
- `Clarify`
- `Correct`

---

## Evaluation Principle

The dataset follows one central principle:

> Artifact quality and artifact validity are separate concepts.

A low-quality artifact should normally remain eligible for evaluation.

A broken or blank artifact may require rejection.

---

## QA

Each record should be checked for:

- Correct schema
- Consistent field values
- Evidence supporting the decision
- Correct rejection handling
- Neutral rubric treatment
- No unsupported conclusions

The dataset is synthetic and intended for portfolio demonstration.
