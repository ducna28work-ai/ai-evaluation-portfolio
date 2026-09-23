# Annotation Error Analysis — Analysis

This directory documents the analysis of annotation disagreements derived from the shared AI Evaluation Benchmark.

## Analysis Objective

The objective is to identify where independent annotations differ, determine whether the disagreement represents an annotation error, and document the reasoning used to resolve the difference.

## Analysis Structure

The analysis follows these stages:

1. Identify annotation disagreements.
2. Compare the judgments from each annotator.
3. Review the evidence used by each annotator.
4. Classify the disagreement.
5. Determine whether an annotation error occurred.
6. Adjudicate the disagreement.
7. Identify potential guideline improvements.
8. Perform a final QA review.

## Comparison Dimensions

The analysis considers:

- Judgment agreement
- Evidence agreement
- Severity agreement
- Rationale quality
- Evaluation dimension consistency
- Requirement coverage

## Error Classification

Disagreements may be classified as:

| Category | Description |
|---|---|
| Criteria Misinterpretation | The evaluation criterion was interpreted incorrectly. |
| Evidence Mismatch | The judgment does not align with observable response evidence. |
| Requirement Omission | An explicit task requirement was overlooked. |
| Severity Inconsistency | The issue was identified but severity was applied inconsistently. |
| Dimension Confusion | The wrong evaluation dimension was applied. |
| Unsupported Judgment | The judgment lacks sufficient evidence or rationale. |

## Adjudication Record

Each reviewed disagreement should contain:

| Field | Description |
|---|---|
| Task ID | Benchmark task identifier |
| Dimension | Evaluation dimension |
| Annotator A | First judgment |
| Annotator B | Second judgment |
| Evidence Comparison | Key evidence differences |
| Error Category | Classified annotation issue |
| Adjudication | Resolved judgment |
| Reasoning | Evidence-based explanation |
| Guideline Action | Recommended clarification, if needed |

## QA Checks

Before finalizing the analysis:

- Confirm that the original task requirements were reviewed.
- Confirm that evidence supports the final judgment.
- Confirm that the correct evaluation dimension was used.
- Confirm that severity is applied consistently.
- Confirm that disagreement classification is documented.
- Confirm that adjudication reasoning is traceable.
- Confirm that any guideline improvement is supported by the observed issue.

## Relationship to the Benchmark

The analysis reuses:

**`../ai-evaluation-benchmark/dataset/benchmark.csv`**

No duplicate benchmark dataset is created for this project.

## Current Status

The analysis framework has been established.

Detailed disagreement records can be added as the benchmark is independently annotated and reviewed.
