# Data Quality Pipeline — Dataset

This directory contains the synthetic input data used to demonstrate the data quality pipeline.

## Dataset Purpose

The dataset is intentionally designed to contain common data quality issues so that the pipeline can demonstrate:

- Detection
- Classification
- Validation
- Correction
- Escalation
- QA

The records are synthetic and created only for portfolio demonstration.

## Expected Schema

| Field | Description |
|---|---|
| `record_id` | Unique record identifier |
| `customer_name` | Customer name |
| `category` | Support category |
| `priority` | Priority level |
| `language` | Customer language |
| `status` | Record status |

## Expected Values

### Category

Allowed examples:

- Billing
- Technical
- Account
- General

### Priority

Allowed values:

- Low
- Medium
- High

### Language

Expected values should follow the defined language labels consistently.

### Status

Allowed examples:

- Open
- Pending
- Resolved

## Intentional Data Quality Issues

The synthetic input data is designed to demonstrate issues such as:

| Issue | Example |
|---|---|
| Missing Value | Required field is empty |
| Invalid Value | Value is outside the allowed set |
| Inconsistent Label | `billing` vs `Billing` |
| Duplicate Record | Same record appears more than once |
| Format Issue | Value does not follow the expected format |

## Processing Principle

The pipeline should not silently modify uncertain data.

Each issue should be:

**Detected → Classified → Validated → Corrected or Escalated → QA Checked**

## Output Expectations

After processing, each issue should have:

- A clear issue classification
- A severity level
- A documented action
- A reason for the action
- A QA status

## Limitations

This dataset is synthetic and intentionally contains errors.

It is not representative of real customer data or a production data-quality environment.
