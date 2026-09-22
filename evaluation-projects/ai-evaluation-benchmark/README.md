# AI Evaluation Benchmark

A synthetic benchmark dataset for structured AI response evaluation across instruction following, factuality, relevance, completeness, response quality, and safety.

## Purpose

This project demonstrates how an evaluation benchmark can be designed as a reusable foundation for annotation and quality-assurance work.

All tasks and responses are synthetic. No proprietary tasks, private data, credentials, or confidential evaluation materials are included.

## Evaluation Dimensions

- Instruction Following
- Factuality
- Relevance
- Completeness
- Response Quality
- Safety

## Record Structure

| Field | Purpose |
|---|---|
| `task_id` | Unique benchmark identifier |
| `dimension` | Primary evaluation dimension |
| `user_prompt` | Synthetic evaluation task |
| `ai_response` | Synthetic model response |
| `judgment` | Evaluation label |
| `evidence` | Observable evidence supporting the judgment |
| `severity` | Impact level of the identified issue |
| `rationale` | Reasoning behind the judgment |
| `qa_status` | Dataset QA status |

## Evaluation Principle

**Task Requirements → Evaluation Criteria → Response Evidence → Judgment → Rationale**

The goal is to make judgments traceable to observable evidence rather than personal preference.

## Dataset Design

The benchmark contains 40 synthetic records across six evaluation dimensions. It intentionally includes both acceptable and problematic responses so it can support later disagreement analysis and comparative evaluation.

## Intended Reuse

This benchmark is the shared foundation for later portfolio projects:

1. **Annotation Error Analysis** — compare independent annotations and analyze disagreement patterns.
2. **Human vs LLM Judge** — compare human-style judgments with an LLM-judge layer.
3. **Data Quality Pipeline** — demonstrate validation and QA on structured evaluation data.

## Limitations

This is a portfolio demonstration dataset, not a production benchmark or scientifically validated evaluation set.

## File

**[→ Open Benchmark CSV](dataset/benchmark.csv)**
