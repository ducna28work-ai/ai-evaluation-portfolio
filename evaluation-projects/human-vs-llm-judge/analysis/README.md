# Human vs LLM Judge — Analysis

This directory documents a synthetic comparison between human-style evaluation judgments and LLM judge judgments using the shared AI Evaluation Benchmark.

## Analysis Objective

The objective is to examine where human-style and LLM judge evaluations agree, where they differ, and what types of errors may occur.

The analysis focuses on evidence and evaluation criteria rather than treating either evaluator as automatically correct.

## Analysis Workflow

**Benchmark → Independent Judgments → Evidence Comparison → Agreement Analysis → Error Classification → Review → QA**

## Comparison Record

Each comparison should contain:

| Field | Description |
|---|---|
| Task ID | Benchmark task identifier |
| Dimension | Evaluation dimension |
| Human Judgment | Human-style evaluation label |
| LLM Judgment | LLM judge evaluation label |
| Human Evidence | Evidence identified by the human-style evaluator |
| LLM Evidence | Evidence identified by the LLM judge |
| Agreement | Agreement classification |
| Error Type | Potential source of disagreement |
| Review | Evidence-based analysis |
| Final Assessment | Result after criteria review |

## Agreement Analysis

The comparison uses four agreement categories:

- **Agreement** — both evaluators reach the same judgment with compatible evidence.
- **Partial Agreement** — judgments differ in strength or severity but rely on similar evidence.
- **Disagreement** — judgments are materially different.
- **Unresolved** — the available evidence does not clearly support one interpretation.

## Judge Error Analysis

Potential LLM judge errors are reviewed using:

| Error Type | Description |
|---|---|
| Criteria Misapplication | Evaluation criteria are applied incorrectly. |
| Evidence Mismatch | The judgment does not match the response evidence. |
| Requirement Omission | An explicit task requirement is overlooked. |
| Unsupported Reasoning | The rationale contains unsupported claims. |
| Severity Inconsistency | Severity is applied inconsistently. |
| Dimension Confusion | The wrong evaluation dimension is used. |

## Review Process

When a human-style and LLM judge evaluation disagree:

1. Re-read the original task.
2. Confirm the evaluation dimension.
3. Compare both judgments.
4. Compare the evidence cited by each evaluator.
5. Review both rationales.
6. Identify the source of disagreement.
7. Determine which judgment is better supported by the documented criteria and evidence.
8. Record the reasoning.
9. Identify potential guideline improvements.

## QA Checks

Before finalizing a comparison:

- Confirm both evaluators assessed the same task.
- Confirm the same evaluation dimension was used.
- Confirm evidence is observable in the response.
- Confirm each judgment has a rationale.
- Confirm disagreement categories are applied consistently.
- Confirm the final assessment is traceable to the evaluation criteria.

## Relationship to the Benchmark

The analysis reuses:

**`../ai-evaluation-benchmark/dataset/benchmark.csv`**

No duplicate benchmark dataset is created.

## Current Status

The analysis framework has been established.

Detailed comparison records will be added using synthetic human-style and LLM judge evaluations derived from the shared benchmark.
