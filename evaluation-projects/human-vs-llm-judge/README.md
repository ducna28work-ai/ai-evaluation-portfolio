# Human vs LLM Judge

A synthetic project demonstrating how human-style evaluation judgments can be compared with judgments produced by an LLM-based judge using a shared evaluation benchmark.

## Purpose

LLM-based judges can be used to support large-scale evaluation, but their judgments should be reviewed for consistency, evidence quality, and alignment with defined evaluation criteria.

This project demonstrates a structured comparison between:

- Human-style evaluation judgments
- LLM judge judgments
- Evidence supporting each judgment
- Agreement and disagreement patterns
- Potential judge errors

The project uses the existing **AI Evaluation Benchmark** rather than creating a separate dataset.

## Data Source

The project reuses:

**[→ AI Evaluation Benchmark](../ai-evaluation-benchmark/)**

The benchmark contains synthetic records across:

- Instruction Following
- Factuality
- Relevance
- Completeness
- Response Quality
- Safety

No proprietary or private evaluation data is used.

## Comparison Workflow

**Benchmark → Human-style Judgment → LLM Judge Judgment → Evidence Comparison → Agreement Analysis → Error Analysis → QA**

## Human-Style Evaluation

The human-style judgment represents an evaluation decision made by applying the documented evaluation criteria and reviewing observable evidence in the response.

The evaluation process follows:

1. Understand the task requirements.
2. Identify the relevant evaluation dimension.
3. Review the response.
4. Identify supporting evidence.
5. Apply the evaluation criteria.
6. Record the judgment.
7. Provide a rationale.

## LLM Judge Evaluation

The LLM judge is treated as a separate evaluation layer.

The judge should:

- Follow the same task requirements.
- Apply the same evaluation dimension.
- Identify observable evidence.
- Produce a structured judgment.
- Provide a rationale.
- Avoid relying on unsupported assumptions.

The LLM judge output should be reviewed against the evaluation criteria rather than treated as automatically correct.

## Comparison Dimensions

The comparison considers:

| Dimension | Purpose |
|---|---|
| Judgment Agreement | Whether both evaluators reach the same judgment |
| Evidence Agreement | Whether they identify similar supporting evidence |
| Rationale Quality | Whether the reasoning is sufficiently supported |
| Criteria Alignment | Whether the evaluation criteria are applied consistently |
| Severity Agreement | Whether issue severity is assessed consistently |
| Error Type | Whether a disagreement can be classified |

## Agreement Categories

Each comparison can be classified as:

- **Agreement** — both evaluators reach the same judgment using compatible evidence.
- **Partial Agreement** — judgments differ in strength or severity but are based on similar evidence.
- **Disagreement** — evaluators reach materially different judgments.
- **Unresolved** — available evidence does not clearly support one interpretation.

## Judge Error Categories

Potential LLM judge errors include:

### Criteria Misapplication

The judge applies the evaluation criterion incorrectly.

### Evidence Mismatch

The judgment does not match the observable evidence in the response.

### Requirement Omission

The judge overlooks an explicit task requirement.

### Unsupported Reasoning

The rationale contains claims that are not supported by the evaluated response.

### Severity Inconsistency

The issue is identified but assigned an inconsistent severity level.

### Dimension Confusion

The judge evaluates the response using the wrong dimension.

## Disagreement Review

When human-style and LLM judge outputs differ:

1. Re-read the original task.
2. Confirm the evaluation dimension.
3. Compare both judgments.
4. Compare the evidence cited by each evaluator.
5. Review the rationales.
6. Identify the source of disagreement.
7. Determine whether the LLM judge or human-style judgment is better supported by the criteria and evidence.
8. Record the reasoning.
9. Identify potential guideline improvements.

The comparison should focus on evidence and evaluation criteria rather than assuming that either evaluation source is automatically correct.

## Quality Assurance

QA checks include:

- Same task requirements used by both evaluators.
- Same evaluation dimension applied.
- Evidence is observable in the response.
- Judgments are supported by rationales.
- Disagreements are documented.
- Judge errors are classified consistently.
- Final conclusions are traceable to the evaluation criteria.

## Key Principle

**Same Task → Same Criteria → Independent Judgments → Evidence Comparison → Agreement Analysis → Error Review**

The objective is to understand when LLM judging aligns with structured human-style evaluation and where additional review may be required.

## Limitations

This is a synthetic portfolio project.

It does not measure the real-world accuracy of a specific LLM judge, nor does it represent production benchmark performance.

The comparison is intended to demonstrate evaluation methodology rather than establish a general performance claim about LLM judges.

## Status

The project structure has been established using the shared AI Evaluation Benchmark.

Detailed human-vs-LLM comparison records will be documented in the `analysis/` directory.
