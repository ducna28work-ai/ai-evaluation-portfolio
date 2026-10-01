# Vietnamese Speech Annotation Dataset

A synthetic dataset designed to demonstrate annotation decisions for spontaneous Vietnamese speech.

## Dataset Objective

The dataset represents the major annotation scenarios defined by the project guideline.

It is intentionally synthetic and does not contain production recordings or confidential project data.

## Coverage

The dataset covers:

1. Basic transcription
2. Written normalization
3. Elongated words
4. Unclear words
5. Inaudible words
6. Foreign-language words
7. Spoken spelling
8. Multiple speakers
9. Speaker overlap
10. Punctuation
11. Pauses
12. Filler words
13. Commonly used words
14. Non-verbal events
15. False starts
16. Repeated complete words
17. Cut-off speech
18. Profanity
19. Dialects
20. Background noise
21. Valid rejection cases
22. Invalid rejection cases
23. QA error cases

## Schema

| Field | Description |
|---|---|
| `annotation_id` | Unique synthetic case ID |
| `scenario` | Annotation scenario |
| `audio_observation` | Description of the synthetic audio |
| `spoken_content` | Spoken content represented by the scenario |
| `expected_transcription` | Expected annotated transcript |
| `rule_applied` | Main guideline rule demonstrated |
| `common_error` | Typical annotation mistake |
| `decision` | Accept or Reject |
| `qa_status` | QA state |

## Decision Values

### Accept

The audio can be annotated using the defined conventions.

### Reject

The primary speaker cannot be understood because of a qualifying audio problem.

## Synthetic Data Principles

The dataset is designed to demonstrate reasoning rather than simulate actual production audio.

Each example should allow a reviewer to answer:

1. What happened in the audio?
2. Which annotation rule applies?
3. What should the transcript contain?
4. What common error should be avoided?
5. Should the audio be accepted or rejected?

## QA Use

The dataset can be used to test:

- Annotation accuracy
- Rule application
- Tag consistency
- Normalization consistency
- Speaker labeling
- Rejection decisions
- Error classification

## Data Quality Principles

A valid annotation should be:

- Faithful to the audio observation.
- Consistent with the defined notation.
- Conservative when speech is uncertain.
- Free from unsupported additions.
- Consistent with rejection rules.

## Limitations

The dataset does not replace real audio review.

Actual speech annotation requires listening to the original recording under the defined listening conditions.
