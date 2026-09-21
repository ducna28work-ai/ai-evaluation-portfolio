# Data Quality Evaluation Example

This example demonstrates how a synthetic dataset can be reviewed for common data quality issues.

The example focuses on:

- Completeness
- Validity
- Consistency
- Uniqueness
- Format compliance
- Annotation quality
- Evidence-based correction decisions

All data in this example is synthetic.

---

## Evaluation Task

Review the following synthetic records and identify any data quality issues.

For each issue:

1. Identify the affected record.
2. Identify the affected field.
3. Classify the issue.
4. Determine severity.
5. Compare the value against the defined data standard.
6. Decide whether the record should be accepted, normalized, corrected, removed, or escalated.
7. Provide a concise rationale.

---

## Data Standard

The dataset uses the following rules.

### Category

Allowed values:

- Billing
- Technical Support
- Account

### Priority

Allowed values:

- Low
- Medium
- High

### Language

Expected values:

- English
- Vietnamese

### Record ID

Each record should have a unique identifier.

### Formatting

Category labels should use consistent capitalization.

---

## Synthetic Records

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

---

# Evaluation

## Record R001

**Finding:** No quality issue detected.

### Validation

- Category: `Billing` → Valid
- Priority: `High` → Valid
- Language: `English` → Valid
- Record ID: Unique

### Decision

**Accept**

### Rationale

All required fields contain valid values and follow the defined dataset standards.

---

## Record R002

**Finding:** No quality issue detected.

### Validation

- Category: `Technical Support` → Valid
- Priority: `Medium` → Valid
- Language: `English` → Valid
- Record ID: Unique

### Decision

**Accept**

### Rationale

The record satisfies the defined schema and value constraints.

---

## Record R003

**Finding:** Missing required value.

### Evidence

The `Priority` field is empty.

### Issue Type

**Completeness Issue**

### Severity

**Major**

### Decision

**Escalate**

### Rationale

Priority is a required field, but there is insufficient information to determine the correct priority without introducing an unsupported value.

---

## Record R004

**Finding:** Invalid value.

### Evidence

The `Priority` value is:

`Urgent`

### Issue Type

**Validity Issue**

### Severity

**Major**

### Decision

**Escalate for correction**

### Rationale

`Urgent` is not included in the defined set of valid priority values.

The evaluator should not automatically replace it with `High` because the available evidence does not establish that `High` is the intended value.

---

## Record R005

**Finding:** Valid record on first occurrence.

### Validation

- Category: `Technical Support` → Valid
- Priority: `Medium` → Valid
- Language: `English` → Valid

### Decision

**Accept provisionally**

### Rationale

The record itself satisfies the defined quality rules.

However, another record with the same Record ID must be checked for duplication.

---

## Record R005 — Duplicate Occurrence

**Finding:** Duplicate record.

### Evidence

The same Record ID appears twice with the same field values.

### Issue Type

**Uniqueness Issue**

### Severity

**Major**

### Decision

**Remove or merge after validation**

### Rationale

The second occurrence appears to duplicate the first record. The evaluator should verify the source before removing a record.

---

## Record R006

**Finding:** Inconsistent label formatting.

### Evidence

The category is:

`billing`

### Expected Standard

`Billing`

### Issue Type

**Consistency Issue**

### Severity

**Minor**

### Decision

**Normalize**

### Rationale

The value appears to represent the valid `Billing` category but does not follow the dataset's capitalization convention.

Unlike the missing priority in R003, the intended normalized representation is unambiguous.

---

## Record R007

**Finding:** Missing required value.

### Evidence

The `Language` field is empty.

### Issue Type

**Completeness Issue**

### Severity

**Major**

### Decision

**Escalate**

### Rationale

Language is required, but the evaluator does not have sufficient evidence to determine whether the correct value is English or Vietnamese.

---

## Record R008

**Finding:** No quality issue detected.

### Validation

- Category: `Account` → Valid
- Priority: `Low` → Valid
- Language: `Vietnamese` → Valid
- Record ID: Unique

### Decision

**Accept**

### Rationale

The record satisfies the defined data quality rules.

---

# Consolidated Findings

| Record | Field | Issue | Severity | Decision |
|---|---|---|---|---|
| R001 | — | No issue | — | Accept |
| R002 | — | No issue | — | Accept |
| R003 | Priority | Missing value | Major | Escalate |
| R004 | Priority | Invalid value | Major | Escalate |
| R005 | — | No issue on first occurrence | — | Accept provisionally |
| R005 | Record ID | Duplicate | Major | Review removal/merge |
| R006 | Category | Inconsistent label | Minor | Normalize |
| R007 | Language | Missing value | Major | Escalate |
| R008 | — | No issue | — | Accept |

---

# Issue Distribution

The dataset contains four types of identified quality issues:

### Completeness

Affected records:

- R003
- R007

### Validity

Affected record:

- R004

### Uniqueness

Affected record:

- R005 duplicate occurrence

### Consistency

Affected record:

- R006

---

# Correction Decisions

The issues should not all be handled in the same way.

| Issue | Action | Reason |
|---|---|---|
| Missing Priority | Escalate | Correct value cannot be safely inferred |
| Invalid Priority | Escalate | Intended replacement is unclear |
| Duplicate Record | Review and remove/merge | Source duplication should be confirmed |
| `billing` label | Normalize to `Billing` | Intended value is unambiguous |

This distinction is important because data quality evaluation should not turn into unsupported data generation.

---

# Final QA

Before accepting the reviewed dataset, perform a final QA pass.

### Detection

- [x] All records reviewed
- [x] Missing values identified
- [x] Invalid values identified
- [x] Duplicate records identified
- [x] Inconsistent labels identified

### Validation

- [x] Findings compared against the defined schema
- [x] Severity assigned consistently
- [x] Evidence documented
- [x] Ambiguous corrections were not invented

### Decision Quality

- [x] Clear issues can be normalized when appropriate
- [x] Uncertain values are escalated
- [x] Duplicate records are reviewed before removal
- [x] Each decision has a rationale

---

# Example Evaluation Record

A structured evaluation record for R004 could look like this:

| Field | Evaluation |
|---|---|
| Record ID | R004 |
| Field | Priority |
| Observed Value | Urgent |
| Expected Standard | Low / Medium / High |
| Issue Type | Invalid Value |
| Severity | Major |
| Decision | Escalate |
| Evidence | `Urgent` is outside the allowed value set |
| Rationale | The intended replacement cannot be determined safely |
| QA Status | Requires Correction |

---

# Key Evaluation Insight

A strong data-quality evaluation does more than identify incorrect records.

It should distinguish between:

**What is clearly wrong**

and

**What the evaluator can safely correct.**

For example:

- `billing` can be normalized to `Billing` because the intended value is clear.
- A missing priority should not automatically be converted into `High` because the correct value is unknown.
- A duplicate should be verified before removal.

This helps maintain data integrity and reduces the risk of introducing new errors during the correction process.

---

# What This Example Demonstrates

This synthetic example demonstrates:

- Record-level data validation
- Schema-based quality checks
- Missing-value detection
- Invalid-value detection
- Duplicate detection
- Label consistency checks
- Severity classification
- Evidence-based decisions
- Correction versus escalation
- Structured QA
- Reproducible evaluation documentation

The example is synthetic and does not represent proprietary, confidential, or production data.
