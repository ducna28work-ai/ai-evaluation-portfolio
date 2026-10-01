# TTS Evaluation Dataset

## Purpose

This dataset contains synthetic records demonstrating pairwise TTS audio evaluation.

Each record represents two anonymous audio outputs generated from the same transcript.

The dataset focuses on:

- Audio and Recording Quality
- Pronunciation Faithfulness
- Naturalness
- Overall Preference
- Dominant Factor
- Evidence
- QA

---

## Dataset Schema

| Field | Description |
|---|---|
| `case_id` | Unique evaluation case |
| `scenario` | Evaluation scenario |
| `transcript` | Shared transcript for A and B |
| `response_a_observation` | Audible observation for A |
| `response_b_observation` | Audible observation for B |
| `audio_quality_a` | Audio and Recording Quality assessment for A |
| `audio_quality_b` | Audio and Recording Quality assessment for B |
| `pronunciation_a` | Pronunciation Faithfulness assessment for A |
| `pronunciation_b` | Pronunciation Faithfulness assessment for B |
| `naturalness_a` | Naturalness assessment for A |
| `naturalness_b` | Naturalness assessment for B |
| `overall_preference` | Preferred response |
| `dominant_factor` | Main factor explaining preference |
| `evidence` | Observable evidence |
| `decision` | Evaluation or rejection decision |
| `qa_status` | QA status |

---

## Allowed Values

### Dimension Assessments

```text
Better
Worse
Comparable
