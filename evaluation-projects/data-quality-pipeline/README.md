# Data Quality Pipeline

A synthetic project demonstrating a structured pipeline for detecting, classifying, validating, correcting, and quality-checking issues in structured evaluation data.

## Purpose

Data quality problems can affect downstream annotation, analysis, and evaluation results.

This project demonstrates a repeatable workflow for processing structured data:

**Raw Data → Validation → Issue Detection → Classification → Correction or Escalation → QA**

The project is designed as a portfolio demonstration of data quality and annotation QA practices.

## Pipeline Stages

### 1. Raw Data

Start with structured records that may contain missing values, invalid values, inconsistent labels, duplicate records, or formatting problems.

### 2. Validation

Check the dataset against expected:

- Schema
- Required fields
- Allowed values
- Data types
- Formatting rules
- Uniqueness requirements

### 3. Issue Detection

Identify records that violate the defined validation rules.

Typical issues include:

- Missing values
- Invalid values
- Inconsistent labels
- Duplicate records
- Schema violations
- Formatting problems

### 4. Issue Classification

Each detected issue is classified by:

- Issue type
- Severity
- Affected field
- Affected record
- Recommended action

### 5. Correction or Escalation

Issues are handled according to their type and severity.

Possible actions include:

- Normalize
- Correct
- Review
- Remove
- Escalate

Corrections should only be made when the intended value can be determined reliably.

### 6. Quality Assurance

After processing, perform a final QA review to confirm:

- Required fields are present.
- Values follow the defined schema.
- Labels are consistent.
- Duplicate records are reviewed.
- Corrections are documented.
- Escalated issues remain traceable.
- The resulting dataset is suitable for downstream use.

## Validation Rules

The pipeline can apply rules such as:

| Rule | Description |
|---|---|
| Required Field | Required fields must contain a valid value. |
| Allowed Value | Categorical fields must use approved labels. |
| Data Type | Values must match the expected data type. |
| Format | Values must follow the required format. |
| Uniqueness | Records requiring unique identifiers must not be duplicated. |
| Consistency | Equivalent labels should use a consistent representation. |

## Issue Severity

Issues can be classified as:

### Minor

The issue does not prevent the record from being interpreted and can be safely normalized.

Example:

`billing` → `Billing`

### Major

The issue materially affects data reliability and requires correction or review.

Examples:

- Invalid categorical value
- Duplicate record
- Missing important field

### Critical

The issue prevents reliable use of the record or indicates a serious structural problem requiring escalation.

## Issue Record

Each detected issue should contain:

| Field | Description |
|---|---|
| Record ID | Identifier of the affected record |
| Field | Field containing the issue |
| Issue Type | Type of data quality problem |
| Severity | Impact level |
| Original Value | Value before correction |
| Corrected Value | Value after correction, if applicable |
| Action | Correction, review, removal, or escalation |
| Reason | Explanation for the action |
| QA Status | Final quality-check status |

## Pipeline Decision Logic

The decision process follows:

**Detect → Classify → Validate → Correct or Escalate → QA**

A correction should not be made simply because another value appears more likely.

When the intended value cannot be established reliably, the record should be escalated for review rather than silently modified.

## Relationship to Existing Data Quality Project

This project is intentionally different from:

**`../data-quality/`**

The existing `data-quality` project demonstrates structured data quality evaluation.

This `data-quality-pipeline` project demonstrates the operational workflow for processing and validating data quality issues.

Both projects therefore serve different purposes and should remain separate.

## Quality Assurance Principles

The pipeline emphasizes:

- Traceability
- Consistency
- Evidence-based correction
- Explicit escalation
- Reproducibility
- Clear documentation
- Final QA validation

## Limitations

This is a synthetic portfolio project.

It demonstrates a data quality workflow but does not represent a production data processing system or proprietary dataset.

## Status

The pipeline framework has been established.

A synthetic dataset and validation analysis can be added to demonstrate the workflow end to end.
