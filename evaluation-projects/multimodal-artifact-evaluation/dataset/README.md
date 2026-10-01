# Multimodal Artifact Evaluation — Dataset

Synthetic dataset demonstrating structured evaluation of AI-generated multimodal artifacts.

## Dataset Purpose

The dataset demonstrates how evaluators can record:

- Artifact type
- Loading state
- Interactive testing
- Rubric results
- Rejection decisions
- Overall preference
- Evidence
- QA status

## Dataset Schema

| Field | Description |
|---|---|
| `evaluation_id` | Unique evaluation identifier |
| `artifact_type` | Type of AI-generated artifact |
| `loading_state_a` | Loading state of Response A |
| `loading_state_b` | Loading state of Response B |
| `rubric_result_a` | Rubric result for Response A |
| `rubric_result_b` | Rubric result for Response B |
| `interaction_test` | Whether relevant interaction was tested |
| `rejection` | Whether the task requires rejection |
| `overall_preference` | Overall comparison |
| `evidence` | Observable evaluation evidence |
| `qa_status` | QA review status |

## Artifact Types

Examples include:

- Website
- Application
- Game
- Visualization
- Presentation
- Report

## Loading States

- Loaded
- Loading
- Broken
- Blank

## Rubric Results

- Good
- Bad

Rubric results are independent for Response A and Response B.

## Rejection

Rejection should only be used when the output is fundamentally unavailable for evaluation according to the applicable rules.

## Data Principles

The dataset emphasizes:

- Independent rubric evaluation
- Evidence-based judgment
- Interactive testing
- Correct rejection handling
- Consistent QA

## Synthetic Data

All records are synthetic and created for portfolio demonstration purposes.
