# TTS Audio Evaluation — Dataset

Synthetic dataset demonstrating structured pairwise evaluation of TTS responses.

## Dataset Purpose

The dataset demonstrates how TTS outputs can be evaluated across:

- Audio and Recording Quality
- Pronunciation Faithfulness
- Naturalness
- Overall Preference

It also includes examples of:

- Close calls
- Both Bad outcomes
- Rejection cases
- Dominant Factor selection
- QA review

## Dataset Schema

| Field | Description |
|---|---|
| `evaluation_id` | Unique evaluation identifier |
| `dimension` | Evaluation dimension |
| `transcript` | Shared transcript |
| `response_a` | Response A identifier |
| `response_b` | Response B identifier |
| `preference` | Selected response |
| `evidence` | Observable reason |
| `dominant_factor` | Main factor affecting overall preference |
| `qa_status` | QA review status |

## Evaluation Dimensions

- Audio and Recording Quality
- Pronunciation Faithfulness
- Naturalness
- Overall Preference

## Preference Values

Depending on the dimension, the dataset can contain:

- A
- B
- Tie
- Both Bad
- Reject

## Data Principles

Each judgment should be:

- Evidence-based
- Dimension-specific
- Consistent with the evaluation rubric
- Independent of speaker identity or target-speaker similarity
- Traceable to an observable quality difference

## Synthetic Data

All records are synthetic examples created for portfolio demonstration.

No production audio, transcript, evaluator identity, or confidential project information is included.
