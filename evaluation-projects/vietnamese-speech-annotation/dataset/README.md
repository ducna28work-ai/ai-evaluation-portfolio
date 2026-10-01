# Vietnamese Speech Annotation — Dataset

Synthetic dataset demonstrating annotation decisions for spontaneous Vietnamese speech.

## Purpose

The dataset is designed to represent common annotation scenarios rather than production audio.

Each record describes an observed synthetic speech event and the expected annotation outcome.

## Dataset Structure

| Field | Description |
|---|---|
| `annotation_id` | Unique annotation identifier |
| `scenario` | Type of speech annotation scenario |
| `audio_observation` | Synthetic description of what can be heard |
| `raw_spoken_form` | Approximate spoken content |
| `expected_transcription` | Expected annotated transcript |
| `annotation_rule` | Rule demonstrated by the example |
| `error_category` | Potential annotation error being tested |
| `rejection_decision` | Accept or Reject |
| `qa_status` | QA review status |

## Scenario Categories

The dataset includes examples covering:

- Standard speech
- Filler words
- Pauses
- Non-verbal sounds
- Unclear words
- Inaudible words
- Foreign-language words
- Spoken spelling
- Multiple speakers
- Speaker overlap
- Numerical normalization
- Dates and times
- Monetary amounts
- Percentages
- Measurements
- False starts
- Cut-off speech
- Dialectal speech
- Profanity
- Background noise
- Rejection cases

## Annotation Principles

### Preserve Speech

Do not rewrite spontaneous speech into polished prose.

### Preserve Meaning

Normalize appropriate written expressions while retaining the meaning of the spoken content.

### Preserve Events

Important non-verbal and disfluency events should be represented using controlled tags.

### Do Not Guess Excessively

Use uncertainty or inaudible tags when the audio does not support a confident transcription.

### Reject Only When Necessary

An understandable audio file should remain annotatable even when it contains noise or other imperfections.

## Synthetic Data Notice

The audio observations and transcripts are fictional examples created for portfolio demonstration.

They are not recordings from real speakers and do not represent production annotation records.
