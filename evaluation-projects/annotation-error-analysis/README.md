# Annotation Error Analysis

A synthetic project demonstrating how annotation disagreements can be identified, classified, analyzed, and resolved using a shared AI evaluation benchmark.

## Purpose

Annotation quality depends not only on having clear evaluation criteria, but also on applying those criteria consistently.

This project demonstrates a structured approach to identifying annotation errors and understanding why independent evaluators may reach different judgments on the same response.

The analysis reuses the shared **AI Evaluation Benchmark** rather than creating a separate dataset.

## Data Source

The project uses the benchmark dataset:

**[→ AI Evaluation Benchmark](../ai-evaluation-benchmark/)**

The benchmark contains synthetic evaluation records covering:

- Instruction Following
- Factuality
- Relevance
- Completeness
- Response Quality
- Safety

No proprietary, private, or confidential annotation data is used.

## Analysis Workflow

**Benchmark Dataset → Independent Annotations → Comparison → Disagreement Detection → Error Classification → Adjudication → Guideline Improvement → QA**

## Annotation Comparison

Two independent annotation sets are conceptually compared against the same benchmark tasks.

The comparison focuses on:

- Judgment agreement
- Judgment disagreement
- Evidence differences
- Severity differences
- Rationale differences
- Interpretation of evaluation criteria

The goal is to distinguish genuine annotation errors from reasonable differences in interpretation.

## Annotation Error Categories

Potential annotation issues are classified into several categories:

### 1. Criteria Misinterpretation

The evaluator applies an evaluation criterion incorrectly or misunderstands what the criterion requires.

### 2. Evidence Mismatch

The judgment does not match the observable evidence in the response.

### 3. Requirement Omission

An explicit task requirement is overlooked during evaluation.

### 4. Severity Inconsistency

The evaluator identifies the issue correctly but assigns an inconsistent severity level.

### 5. Dimension Confusion

The evaluator applies the wrong evaluation dimension to the observed issue.

### 6. Unsupported Judgment

The evaluator provides a judgment without sufficient evidence or rationale.

## Disagreement Analysis

For each disagreement, the analysis should identify:

| Field | Description |
|---|---|
| Task ID | Benchmark record being reviewed |
| Evaluation Dimension | Dimension being assessed |
| Annotator A | First annotation |
| Annotator B | Second annotation |
| Evidence A | Evidence used by Annotator A |
| Evidence B | Evidence used by Annotator B |
| Disagreement Type | Type of disagreement |
| Error Classification | Identified annotation issue |
| Adjudication | Final resolution |
| Guideline Action | Whether the guideline should be clarified |

## Adjudication

When annotators disagree, the resolution process follows:

1. Re-read the original task requirements.
2. Identify the evaluation dimension being applied.
3. Review the response evidence.
4. Compare the evidence used by each annotator.
5. Determine whether one judgment violates the evaluation criteria.
6. Resolve the disagreement using the documented criteria.
7. Record the reasoning behind the resolution.
8. Identify whether the guideline needs clarification.

Adjudication should focus on the evaluation criteria and observable evidence rather than personal preference.

## Guideline Improvement

Repeated disagreement patterns can indicate that an evaluation guideline needs clarification.

Potential improvements include:

- Adding clearer decision rules
- Defining ambiguous terms
- Adding positive and negative examples
- Clarifying severity thresholds
- Adding edge cases
- Separating commonly confused evaluation dimensions

The purpose is not only to resolve individual disagreements, but also to reduce similar disagreements in future annotation rounds.

## Quality Assurance

The final QA review checks:

- All disagreements have been reviewed.
- Each resolution is supported by evidence.
- Error categories are applied consistently.
- Severity labels follow the defined criteria.
- Adjudication decisions are documented.
- Guideline improvements are traceable to observed issues.

## Key Principle

**Disagreement → Evidence Review → Error Classification → Adjudication → Guideline Improvement**

The objective is to turn annotation disagreements into measurable quality-improvement opportunities.

## Limitations

This is a synthetic portfolio project designed to demonstrate annotation QA methodology.

It does not represent production annotation statistics or proprietary evaluation workflows.

## Status

The project structure is established using the shared AI Evaluation Benchmark.

Detailed disagreement and error analysis will be developed in the `analysis/` directory.
