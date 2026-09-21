# Data Quality Evaluation Project

This project demonstrates a structured approach to evaluating the quality of synthetic annotated data.

The goal is to identify data quality issues, classify their severity, determine whether records can be corrected, and perform a final quality check before accepting the dataset.

All data in this project is synthetic and created for portfolio demonstration purposes.

---

## Objective

Evaluate a small synthetic dataset for common data quality issues, including:

- Missing values
- Invalid values
- Inconsistent labels
- Duplicate records
- Format and schema problems
- Annotation errors
- Inconsistent data representation

The evaluation follows a structured workflow:

**Detect → Classify → Validate → Correct or Escalate → QA**

---

## Synthetic Dataset

The dataset contains records representing annotated customer-support examples.

| Record ID | Category | Priority | Language | Annotation Status |
|---|---|---|---|---|
| R001 | Billing | High | English | Valid |
| R002 | Technical Support | Medium | English | Valid |
| R003 | Billing |  | English | Missing Priority |
| R004 | Technical Support | Urgent | English | Invalid Priority |
| R005 | Technical Support | Medium | English | Valid |
| R005 | Technical Support | Medium | English | Duplicate Record |
| R006 | billing | High | English | Inconsistent Label |
| R007 | Account | Low |  | Missing Language |
| R008 | Account | Low | Vietnamese | Valid |

---

## Evaluation Criteria

Each record is reviewed against the following dimensions.

### 1. Completeness

Check whether all required fields contain values.

Examples:

- Missing priority
- Missing language
- Missing category

A missing required value is recorded as a data quality issue.

---

### 2. Validity

Check whether values conform to the allowed values or expected data rules.

For example:

**Allowed Priority Values**

- Low
- Medium
- High

A value such as `Urgent` is invalid when it is not part of the defined schema.

---

### 3. Consistency

Check whether equivalent values are represented consistently.

For example:

- `Billing`
- `billing`

These values may represent the same category but use inconsistent formatting.

---

### 4. Uniqueness

Check whether records are duplicated.

A duplicate record should be identified before the dataset is accepted.

---

### 5. Format Compliance

Check whether values follow the expected representation.

Examples:

- Consistent capitalization
- Expected field structure
- Valid category names
- Valid priority values

---

### 6. Annotation Consistency

Check whether annotations follow the same labeling rules across records.

Inconsistent annotation can reduce the reliability of downstream evaluation or machine-learning workflows.

---

## Record-Level Evaluation

### R001

**Status:** Valid

**Findings:**

- Category: Valid
- Priority: Valid
- Language: Valid
- No duplicate detected

**Decision:** Accept

---

### R002

**Status:** Valid

**Findings:**

- Category: Valid
- Priority: Valid
- Language: Valid
- No duplicate detected

**Decision:** Accept

---

### R003

**Status:** Quality Issue

**Issue:** Missing required value

**Field:** Priority

**Severity:** Major

**Decision:** Escalate for correction

**Rationale:** The priority field is required but contains no value. The correct value cannot be inferred safely from the record alone.

---

### R004

**Status:** Quality Issue

**Issue:** Invalid value

**Field:** Priority

**Value:** `Urgent`

**Severity:** Major

**Decision:** Escalate for correction

**Rationale:** `Urgent` is outside the defined priority values of Low, Medium, and High.

---

### R005 — First Occurrence

**Status:** Valid

**Findings:**

- Category: Valid
- Priority: Valid
- Language: Valid

**Decision:** Accept provisionally

---

### R005 — Second Occurrence

**Status:** Quality Issue

**Issue:** Duplicate record

**Severity:** Major

**Decision:** Remove or merge after validation

**Rationale:** The record ID and field values match the first R005 record.

---

### R006

**Status:** Quality Issue

**Issue:** Inconsistent label

**Field:** Category

**Value:** `billing`

**Expected representation:** `Billing`

**Severity:** Minor

**Decision:** Normalize

**Rationale:** The value appears to represent the same category but does not follow the dataset's capitalization convention.

---

### R007

**Status:** Quality Issue

**Issue:** Missing required value

**Field:** Language

**Severity:** Major

**Decision:** Escalate for correction

**Rationale:** The language field is missing and cannot be safely inferred from the available record.

---

### R008

**Status:** Valid

**Findings:**

- Category: Valid
- Priority: Valid
- Language: Valid
- No duplicate detected

**Decision:** Accept

---

## Issue Summary

| Issue Type | Records | Severity | Recommended Action |
|---|---|---|---|
| Missing value | R003, R007 | Major | Correct or escalate |
| Invalid value | R004 | Major | Correct or escalate |
| Duplicate | R005 | Major | Remove or merge after validation |
| Inconsistent label | R006 | Minor | Normalize |

---

## Correction and Escalation Logic

Not every quality issue should be automatically corrected.

### Safe to Normalize

A value may be normalized when the intended value is unambiguous.

Example:

`billing` → `Billing`

This is a formatting consistency issue.

### Requires Validation

A value should not be changed automatically when multiple interpretations are possible.

Example:

Missing priority in R003.

The evaluator should not invent a priority simply to make the dataset complete.

### Requires Removal or Deduplication Review

Duplicate records should be reviewed before deletion.

The evaluator should verify that the records are genuinely duplicates rather than separate records with similar content.

---

## Final QA Check

After identifying the issues, perform a second quality review.

### QA Checklist

- [x] All records were reviewed
- [x] Missing required fields were identified
- [x] Invalid values were identified
- [x] Inconsistent labels were identified
- [x] Duplicate records were identified
- [x] Issues were classified by severity
- [x] Corrections were separated from escalation decisions
- [x] No unsupported values were invented
- [x] Final findings were documented

---

## Final Assessment

The dataset contains several quality issues that should be resolved before being considered fully ready for downstream use.

The main issues are:

1. Missing required values
2. An invalid priority value
3. A duplicate record
4. An inconsistent category label

The evaluation also demonstrates an important quality-control principle:

**A data evaluator should identify and document uncertainty rather than inventing missing information.**

---

## Evaluation Record Structure

A reusable evaluation record can follow this structure:

| Field | Description |
|---|---|
| Record ID | Identifier of the evaluated record |
| Field | Field containing the issue |
| Issue Type | Category of data quality issue |
| Evidence | Observed value or condition |
| Expected Standard | Relevant schema or quality rule |
| Severity | Minor, Major, or Critical |
| Decision | Accept, Normalize, Correct, Remove, or Escalate |
| Rationale | Reason supporting the decision |
| QA Status | Whether the issue was resolved or requires review |

---

## Key Principles

### 1. Validate Before Correcting

Identify the issue and determine whether the intended correction is supported by available evidence.

### 2. Do Not Invent Missing Data

Missing information should remain unresolved when there is insufficient evidence to determine the correct value.

### 3. Separate Detection From Correction

Finding a quality issue does not automatically mean the evaluator should modify the data.

### 4. Apply Consistent Rules

The same validation criteria should be applied across records.

### 5. Document Evidence

Every quality decision should be traceable to an observed value, schema rule, or validation condition.

### 6. Perform a Final QA Pass

A second review helps identify missed issues and confirms that corrections follow the defined quality rules.

---

## What This Project Demonstrates

This project demonstrates practical capabilities in:

- Data quality evaluation
- Structured annotation review
- Dataset validation
- Error classification
- Missing-value detection
- Invalid-value detection
- Duplicate detection
- Label consistency checks
- Correction and escalation decisions
- Evidence-based QA
- Structured documentation

The project is intentionally synthetic and does not represent proprietary or confidential production data.
