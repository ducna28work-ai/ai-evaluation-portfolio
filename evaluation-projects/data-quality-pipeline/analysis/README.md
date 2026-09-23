# Data Quality Pipeline — Analysis

This directory documents the validation and processing results from the synthetic data quality pipeline dataset.

## Analysis Objective

The objective is to demonstrate how structured records can be validated, issues can be detected and classified, and appropriate correction or escalation decisions can be documented.

## Processing Workflow

**Raw Data → Validation → Issue Detection → Classification → Correction or Escalation → QA**

## Validation Results

The synthetic dataset contains both valid and problematic records.

| Record ID | Field | Issue | Severity | Action |
|---|---|---|---|---|
| P001 | — | No issue detected | — | Keep |
| P002 | — | No issue detected | — | Keep |
| P003 | Priority | Missing value | Major | Escalate |
| P004 | Priority | Invalid value: `Urgent` | Major | Escalate |
| P005 | Record | Duplicate record | Major | Review for Removal or Merge |
| P006 | Category | Inconsistent label: `billing` | Minor | Normalize to `Billing` |
| P007 | Language | Missing value | Major | Escalate |
| P008 | — | No issue detected | — | Keep |
| P009 | — | No issue detected | — | Keep |
| P010 | — | No issue detected | — | Keep |
| P011 | — | No issue detected | — | Keep |

## Issue Classification

### P003 — Missing Priority

**Issue Type:** Missing Value

**Severity:** Major

**Action:** Escalate

**Reason:** The priority field is expected to contain a valid value, but the intended priority cannot be determined from the record alone.

---

### P004 — Invalid Priority

**Issue Type:** Invalid Value

**Severity:** Major

**Original Value:** `Urgent`

**Action:** Escalate

**Reason:** `Urgent` is not part of the defined priority values. The correct replacement cannot be determined reliably from the available record.

---

### P005 — Duplicate Record

**Issue Type:** Duplicate

**Severity:** Major

**Action:** Review for Removal or Merge

**Reason:** The same record appears twice. A review is required before removing or merging the duplicate.

---

### P006 — Inconsistent Category

**Issue Type:** Inconsistent Label

**Severity:** Minor

**Original Value:** `billing`

**Corrected Value:** `Billing`

**Action:** Normalize

**Reason:** The value represents the same category but uses inconsistent capitalization.

---

### P007 — Missing Language

**Issue Type:** Missing Value

**Severity:** Major

**Action:** Escalate

**Reason:** The language field is empty and the correct value cannot be established reliably from the available record.

## Correction vs Escalation

The pipeline distinguishes between issues that can be safely normalized and issues that require human review.

### Safe Correction

P006 can be normalized because:

`billing` → `Billing`

does not change the underlying category.

### Escalation

P003, P004, and P007 should be escalated because the intended values cannot be determined reliably.

P005 requires review because duplicate handling depends on the intended record-management policy.

## QA Review

After processing, the following checks should be performed:

- Required fields have been reviewed.
- Invalid categorical values have been identified.
- Duplicate records have been flagged.
- Label inconsistencies have been normalized where safe.
- Uncertain values have not been silently invented.
- Escalated records remain traceable.
- Every identified issue has a documented action.

## Pipeline Outcome

The synthetic dataset demonstrates the complete processing logic:

**Detect → Classify → Validate → Correct or Escalate → QA**

The key principle is that data correction should be evidence-based. When the intended value cannot be established reliably, escalation is preferable to unsupported modification.

## Relationship to the Input Dataset

The analysis is based on:

**`../dataset/data_quality_pipeline.csv`**

The dataset is synthetic and intentionally contains quality issues for demonstration purposes.

## Limitations

This is a portfolio demonstration rather than a production data-quality system.

The dataset is small and synthetic, so the workflow should not be interpreted as evidence of production-scale processing performance.
