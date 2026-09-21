# Data Quality Evaluation Dataset

This dataset contains synthetic records for demonstrating structured data quality evaluation and annotation QA.

The dataset follows the workflow:

**Record → Validation Rule → Evidence → Issue Classification → Severity → Decision → QA**

All records are synthetic and created for portfolio demonstration purposes.

---

## Dataset Purpose

This dataset demonstrates how structured records can be reviewed for common data quality issues.

The evaluation covers:

- Completeness
- Validity
- Consistency
- Uniqueness
- Format Compliance
- Annotation Consistency
- Missing-value handling
- Duplicate detection
- Correction and escalation decisions

---

## Data Schema

The synthetic dataset represents customer-support records.

| Field | Description | Required |
|---|---|---|
| Record ID | Unique record identifier | Yes |
| Category | Support category | Yes |
| Priority | Request priority | Yes |
| Language | Customer language | Yes |

### Allowed Category Values

- Billing
- Technical Support
- Account

### Allowed Priority Values

- Low
- Medium
- High

### Allowed Language Values

- English
- Vietnamese

---

# Synthetic Dataset

| Record ID | Category | Priority | Language |
|---|---|---|---|
| R001 | Billing | High | English |
| R002 | Technical Support | Medium | English |
| R003 | Billing |  | English |
| R004 | Technical Support | Urgent | English |
| R005 | Technical Support | Medium | English |
| R005 | Technical Support | Medium | English |
| R006 | billing | High | English |
| R007 | Account | Low |  |
| R008 | Account | Low | Vietnamese |
| R009 | Technical Support | High | Vietnamese |

---

# Record-Level Evaluation

## R001

**Finding:** No quality issue.

**Validation:**

- Record ID: Unique
- Category: Valid
- Priority: Valid
- Language: Valid

**Issue Type:** None

**Severity:** N/A

**Decision:** Accept

**Rationale:** All required fields contain valid values and follow the defined schema.

**QA Status:** Passed

---

## R002

**Finding:** No quality issue.

**Validation:**

- Record ID: Unique
- Category: Valid
- Priority: Valid
- Language: Valid

**Issue Type:** None

**Severity:** N/A

**Decision:** Accept

**Rationale:** The record satisfies the defined data quality rules.

**QA Status:** Passed

---

## R003

**Finding:** Missing required value.

**Affected Field:** Priority

**Observed Value:** Empty

**Expected Standard:** Low / Medium / High

**Issue Type:** Completeness

**Severity:** Major

**Decision:** Escalate

**Evidence:** The required Priority field contains no value.

**Rationale:** The correct priority cannot be determined safely from the available information.

**QA Status:** Requires Correction

---

## R004

**Finding:** Invalid value.

**Affected Field:** Priority

**Observed Value:** `Urgent`

**Expected Standard:** Low / Medium / High

**Issue Type:** Validity

**Severity:** Major

**Decision:** Escalate

**Evidence:** `Urgent` is outside the defined priority values.

**Rationale:** The evaluator cannot determine whether the intended priority is Low, Medium, or High.

**QA Status:** Requires Correction

---

## R005 — First Occurrence

**Finding:** Valid record.

**Validation:**

- Record ID: Valid
- Category: Valid
- Priority: Valid
- Language: Valid

**Issue Type:** None

**Severity:** N/A

**Decision:** Accept Provisionally

**Rationale:** The record satisfies the schema, but another record with the same identifier requires duplicate validation.

**QA Status:** Requires Duplicate Check

---

## R005 — Second Occurrence

**Finding:** Duplicate record.

**Affected Field:** Record ID

**Observed Value:** `R005`

**Issue Type:** Uniqueness

**Severity:** Major

**Decision:** Review for Removal or Merge

**Evidence:** The same Record ID and field values appear in another record.

**Rationale:** The second record appears to duplicate the first occurrence. The source should be checked before removal.

**QA Status:** Requires Review

---

## R006

**Finding:** Inconsistent label representation.

**Affected Field:** Category

**Observed Value:** `billing`

**Expected Standard:** `Billing`

**Issue Type:** Consistency

**Severity:** Minor

**Decision:** Normalize

**Evidence:** The category uses lowercase formatting while the defined category value uses title case.

**Rationale:** The intended category is unambiguous and can be normalized without changing its meaning.

**QA Status:** Correctable

---

## R007

**Finding:** Missing required value.

**Affected Field:** Language

**Observed Value:** Empty

**Expected Standard:** English / Vietnamese

**Issue Type:** Completeness

**Severity:** Major

**Decision:** Escalate

**Evidence:** The required Language field contains no value.

**Rationale:** There is insufficient evidence to determine the correct language.

**QA Status:** Requires Correction

---

## R008

**Finding:** No quality issue.

**Validation:**

- Record ID: Unique
- Category: Valid
- Priority: Valid
- Language: Valid

**Issue Type:** None

**Severity:** N/A

**Decision:** Accept

**Rationale:** All required fields contain valid values.

**QA Status:** Passed

---

## R009

**Finding:** No quality issue.

**Validation:**

- Record ID: Unique
- Category: Valid
- Priority: Valid
- Language: Valid

**Issue Type:** None

**Severity:** N/A

**Decision:** Accept

**Rationale:** The record conforms to the defined schema and allowed values.

**QA Status:** Passed

---

# Consolidated Evaluation

| Record | Issue Type | Severity | Decision | QA Status |
|---|---|---|---|---|
| R001 | None | — | Accept | Passed |
| R002 | None | — | Accept | Passed |
| R003 | Completeness | Major | Escalate | Requires Correction |
| R004 | Validity | Major | Escalate | Requires Correction |
| R005 | None / Duplicate Review | Major | Review | Requires Review |
| R006 | Consistency | Minor | Normalize | Correctable |
| R007 | Completeness | Major | Escalate | Requires Correction |
| R008 | None | — | Accept | Passed |
| R009 | None | — | Accept | Passed |

---

# Issue Distribution

The dataset contains:

| Issue Type | Affected Records | Severity |
|---|---|---|
| Missing Value | R003, R007 | Major |
| Invalid Value | R004 | Major |
| Duplicate | R005 | Major |
| Inconsistent Label | R006 | Minor |

---

# Decision Logic

## Accept

Use when all required values are valid and the record satisfies the schema.

Examples:

- R001
- R002
- R008
- R009

---

## Normalize

Use when the value clearly represents an accepted value but does not follow the required representation.

Example:

`billing` → `Billing`

The correction is unambiguous.

---

## Escalate

Use when a required value is missing or invalid and the correct replacement cannot be determined from available evidence.

Examples:

- Missing priority
- Invalid priority
- Missing language

---

## Review Duplicate

A duplicate should be validated before removal.

The evaluator should not automatically delete a record solely because it appears similar to another record.

---

# Quality Assurance

Each record was reviewed against the same schema and validation rules.

### Completeness

- [x] Required fields identified
- [x] Missing values detected
- [x] Missing values not replaced without evidence

### Validity

- [x] Category values checked
- [x] Priority values checked
- [x] Language values checked

### Consistency

- [x] Category representation reviewed
- [x] Normalization opportunity identified

### Uniqueness

- [x] Record IDs reviewed
- [x] Duplicate R005 identified

### Decision Quality

- [x] Evidence documented
- [x] Severity assigned
- [x] Correction separated from escalation
- [x] Ambiguous values were not invented

---

# Annotation Principles

### Evidence Before Correction

Identify the quality issue before deciding whether a correction is appropriate.

### Do Not Invent Missing Data

A missing value should not be replaced simply because one option appears likely.

### Normalize Only When Unambiguous

Formatting inconsistencies can be corrected when the intended value is clear.

### Validate Duplicates

Potential duplicates should be reviewed before deletion or merging.

### Apply Consistent Rules

Every record should be evaluated using the same schema and validation criteria.

---

# Dataset Summary

This synthetic dataset contains:

- 9 records
- 4 identified issue types
- 3 major issue categories
- 1 minor consistency issue
- Valid and invalid examples
- Correction and escalation cases
- Duplicate detection
- Record-level evidence
- Structured QA decisions

The dataset demonstrates a complete data quality workflow:

**Detect → Classify → Validate → Correct or Escalate → QA**

No private, proprietary, confidential, or personally identifiable information is included.
