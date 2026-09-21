# Data Quality Evaluation Rubric

This rubric provides reusable criteria for evaluating the quality of structured datasets and annotated records.

It is designed to support consistent, evidence-based review across data annotation and data quality tasks.

All examples are synthetic.

---

## Evaluation Dimensions

Data quality should be evaluated across multiple dimensions rather than using a single overall judgment.

### 1. Completeness

Determine whether all required fields contain appropriate values.

| Rating | Description |
|---|---|
| Complete | All required fields are populated |
| Mostly Complete | Minor non-critical information is missing |
| Partially Complete | One or more important fields are missing |
| Incomplete | Multiple required fields are missing or the record cannot be reliably used |

---

### 2. Validity

Determine whether values conform to the defined schema, allowed values, or validation rules.

| Rating | Description |
|---|---|
| Valid | All values conform to the defined rules |
| Minor Validity Issue | A non-critical formatting or representation issue exists |
| Major Validity Issue | One or more important values violate the defined rules |
| Critical Validity Issue | The record cannot be reliably interpreted or used |

---

### 3. Consistency

Determine whether equivalent values are represented consistently.

Examples:

- `Billing` vs `billing`
- Different date formats
- Different label conventions
- Inconsistent annotation terminology

| Rating | Description |
|---|---|
| Consistent | Values follow the same representation rules |
| Minor Inconsistency | Small formatting difference with clear intended meaning |
| Major Inconsistency | Inconsistency may affect interpretation or downstream processing |
| Critical Inconsistency | Data cannot be reliably interpreted because of inconsistent representation |

---

### 4. Uniqueness

Determine whether records are duplicated when unique records are expected.

| Rating | Description |
|---|---|
| Unique | No duplicate detected |
| Potential Duplicate | Similarity suggests duplication but requires validation |
| Duplicate | Evidence confirms the record is duplicated |

---

### 5. Format Compliance

Determine whether values follow the expected representation.

Examples:

- Correct capitalization
- Valid identifier format
- Correct field structure
- Expected date format
- Valid categorical values

---

### 6. Annotation Consistency

Determine whether labels or annotations follow the same rules across records.

The evaluator should check whether equivalent cases receive equivalent labels and whether annotation decisions are supported by the defined guidelines.

---

# Issue Types

Use standardized issue categories whenever possible.

| Issue Type | Description |
|---|---|
| Missing Value | A required field contains no value |
| Invalid Value | A value violates the allowed schema or value set |
| Inconsistent Label | Equivalent labels use inconsistent representations |
| Duplicate Record | The same record appears more than once |
| Format Error | A value does not follow the expected format |
| Annotation Error | A label or annotation does not follow the defined rule |
| Schema Error | The record does not conform to the expected structure |
| Unsupported Value | A value cannot be validated against the available rules |

---

# Severity

Severity should reflect the potential impact of the issue.

## Minor

Use when the issue has limited impact and the intended correction is clear.

Examples:

- Capitalization inconsistency
- Non-critical formatting issue
- Clear normalization opportunity

---

## Major

Use when the issue affects data reliability or requires correction or review.

Examples:

- Missing required field
- Invalid categorical value
- Confirmed duplicate
- Incorrect annotation

---

## Critical

Use when the issue substantially prevents the record or dataset from being safely used.

Examples:

- Corrupted structure
- Severe schema failure
- Systematic annotation failure
- Data that cannot be reliably interpreted

---

# Decision Types

After identifying an issue, determine the appropriate action.

| Decision | When to Use |
|---|---|
| Accept | No meaningful quality issue detected |
| Normalize | Value is clearly correctable through standard normalization |
| Correct | Evidence supports a specific correction |
| Remove | Record is confirmed invalid or duplicated and removal is justified |
| Merge | Duplicate or fragmented records should be combined after validation |
| Escalate | Correct value or action cannot be safely determined |
| Reject | Data fails required quality standards and should not proceed |

---

# Evidence Standard

Every quality finding should be supported by observable evidence.

Strong evidence includes:

- The actual field value
- The defined schema
- Allowed-value list
- Annotation guideline
- Duplicate identifier
- Validation rule
- Documented formatting standard

Avoid unsupported statements such as:

> “This value is probably wrong.”

Prefer:

> “The value `Urgent` is outside the allowed priority values of Low, Medium, and High.”

The second statement identifies both the evidence and the applicable standard.

---

# Missing-Value Rules

When a required value is missing:

### Step 1

Confirm that the field is actually required.

### Step 2

Record the missing value as a completeness issue.

### Step 3

Determine whether the correct value can be established from available evidence.

### Step 4

If the value cannot be established safely, escalate rather than inventing a replacement.

### Key Principle

**Do not fabricate missing data to make a dataset appear complete.**

---

# Invalid-Value Rules

When a value does not conform to the allowed values:

1. Record the observed value.
2. Identify the expected value set.
3. Determine whether the intended correction is unambiguous.
4. Normalize or correct only when supported by evidence.
5. Escalate when multiple possible corrections exist.

Example:

Observed:

`Urgent`

Allowed:

- Low
- Medium
- High

Decision:

**Escalate**

Reason:

The evaluator cannot determine whether the intended value is Low, Medium, or High from the available information.

---

# Duplicate Rules

When a possible duplicate is detected:

1. Compare record identifiers.
2. Compare relevant field values.
3. Determine whether the records represent the same underlying item.
4. Confirm duplication before removing data.
5. Document the decision.

A similar record is not automatically a duplicate.

---

# Normalization Rules

Normalization is appropriate when the intended representation is unambiguous.

Example:

`billing` → `Billing`

This can be normalized when `Billing` is the defined category and no alternative interpretation exists.

Normalization should not be used to guess missing or ambiguous information.

---

# Annotation Quality Rules

For annotated datasets, evaluate:

- Label correctness
- Label consistency
- Guideline adherence
- Ambiguous cases
- Missing annotations
- Unsupported annotations
- Boundary cases

When an annotation guideline does not clearly resolve a case, record the ambiguity rather than forcing an unsupported label.

---

# Quality Assessment Template

Use the following structure for individual findings:

| Field | Description |
|---|---|
| Record ID | Identifier of the record |
| Field | Affected field |
| Observed Value | Value found in the record |
| Expected Standard | Applicable rule or allowed value |
| Issue Type | Type of quality issue |
| Severity | Minor, Major, or Critical |
| Evidence | Observable evidence |
| Decision | Accept, Normalize, Correct, Remove, Merge, Escalate, or Reject |
| Rationale | Explanation for the decision |
| QA Status | Resolved, Pending Review, or Rejected |

---

# Dataset-Level Assessment

After reviewing individual records, summarize the dataset as a whole.

Consider:

- Number of records reviewed
- Number of valid records
- Number of affected records
- Issue types detected
- Severity distribution
- Records requiring correction
- Records requiring escalation
- Remaining unresolved issues

A dataset should not be considered fully acceptable simply because most records are valid.

Systematic issues affecting a smaller number of records may still require investigation.

---

# Quick Decision Guide

### Is the value missing?

→ Check whether the field is required.

If required:

→ Record a completeness issue.

→ If the correct value is unknown, **Escalate**.

---

### Is the value outside the allowed set?

→ Record a validity issue.

→ Check whether the intended correction is unambiguous.

If unclear:

→ **Escalate**.

---

### Is the value formatted differently?

→ Check whether the intended normalized representation is clear.

If yes:

→ **Normalize**.

If no:

→ **Escalate**.

---

### Is the record duplicated?

→ Validate the duplication first.

If confirmed:

→ **Remove or Merge** according to the dataset rules.

---

### Is the annotation inconsistent?

→ Compare the annotation against the applicable guideline and similar records.

If the correct label is clear:

→ **Correct**.

If the guideline does not resolve the case:

→ **Escalate**.

---

# Quality Assurance Checklist

Before finalizing an evaluation:

- [ ] All records were reviewed
- [ ] Required fields were identified
- [ ] Missing values were recorded
- [ ] Invalid values were checked against the schema
- [ ] Duplicate records were investigated
- [ ] Label consistency was reviewed
- [ ] Annotation rules were applied consistently
- [ ] Severity was assigned using the defined criteria
- [ ] Evidence was recorded for each finding
- [ ] Corrections were separated from assumptions
- [ ] Ambiguous cases were escalated
- [ ] A final QA pass was completed

---

# Common Evaluation Errors

## 1. Inventing Missing Values

Incorrect approach:

> Assigning a value because it seems likely.

Correct approach:

> Record the missing value and escalate when evidence is insufficient.

---

## 2. Treating Similar Records as Automatically Duplicate

Similarity alone does not prove duplication.

The evaluator should compare relevant identifiers and fields before deciding.

---

## 3. Correcting Without Evidence

A correction should be supported by the schema, annotation guideline, or other available evidence.

---

## 4. Ignoring Minor Consistency Issues

Minor issues may not prevent immediate use, but identifying them helps maintain standardized datasets.

---

## 5. Using Different Standards Across Records

The same quality rules should be applied consistently throughout the evaluation.

---

# Reusable Evaluation Record

A compact evaluation record can follow this format:

**Record ID:**  
**Field:**  
**Observed Value:**  
**Expected Standard:**  
**Issue Type:**  
**Severity:**  
**Evidence:**  
**Decision:**  
**Rationale:**  
**QA Status:**

---

# Key Principles

1. **Evaluate against defined standards.**
2. **Use observable evidence.**
3. **Separate detection from correction.**
4. **Do not invent missing information.**
5. **Normalize only when the intended value is clear.**
6. **Validate duplicates before removing them.**
7. **Apply the same rules consistently.**
8. **Escalate ambiguity instead of guessing.**
9. **Document every important decision.**
10. **Perform a final QA review.**

---

## What This Rubric Demonstrates

This rubric provides a reusable structure for:

- Data quality evaluation
- Dataset validation
- Annotation QA
- Error classification
- Record-level review
- Schema validation
- Missing-value handling
- Duplicate detection
- Label consistency checks
- Correction and escalation decisions
- Evidence-based quality assurance
