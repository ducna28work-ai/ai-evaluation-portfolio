# Evaluation Datasets

This directory contains synthetic datasets created to demonstrate structured AI evaluation and data quality workflows.

The datasets are designed to show how evaluation records can be structured around:

**Task / Record → Criteria → Evidence → Judgment → Rationale → QA**

All datasets are synthetic and created for portfolio demonstration purposes.

---

## Available Datasets

### Response Evaluation Dataset

A synthetic dataset containing AI response evaluation records across multiple evaluation dimensions.

It demonstrates:

- Instruction Following
- Factuality & Accuracy
- Relevance
- Completeness
- Response Quality
- Safety & Policy Compliance
- Evidence-based judgment
- Structured annotation
- Quality Assurance

**[→ View Response Evaluation Dataset](response-evaluation/)**

**[→ Open CSV Dataset](response-evaluation/response_evaluation.csv)**

---

### Data Quality Evaluation Dataset

A synthetic dataset containing structured records evaluated for common data quality issues.

It demonstrates:

- Completeness
- Validity
- Consistency
- Uniqueness
- Format Compliance
- Missing-value handling
- Duplicate detection
- Correction and escalation
- Data quality assurance

**[→ View Data Quality Dataset](data-quality/)**

**[→ Open CSV Dataset](data-quality/data_quality.csv)**

---

## Dataset Design Principles

### Evidence Before Judgment

Evaluation decisions should be supported by observable evidence.

### Consistent Criteria

Comparable records should be evaluated using the same defined criteria.

### Structured Annotation

Each record should contain enough information to understand how the evaluation decision was reached.

### Explicit Rationale

Judgments should include a concise explanation of why the evidence supports the decision.

### Quality Assurance

Each evaluation should include a final QA check before being considered complete.

### No Unsupported Corrections

Missing or ambiguous information should not be invented simply to make a dataset appear complete.

---

## Dataset Workflow

### AI Response Evaluation

**Task → Response → Criteria → Evidence → Judgment → Rationale → QA**

### Data Quality Evaluation

**Record → Validation Rule → Evidence → Issue Classification → Severity → Decision → QA**

---

## Dataset Scope

These datasets are intended to demonstrate:

- Evaluation methodology
- Annotation structure
- Evidence-based decision making
- Quality-control workflows
- Reproducible evaluation practices

They are not intended to represent production benchmark datasets.

---

## Confidentiality

All records are synthetic.

The datasets contain no:

- Private evaluation tasks
- Proprietary benchmark data
- Confidential company information
- Personally identifiable information
- Credentials
- Production customer data

---

## Current Dataset Inventory

| Dataset | Records | Format | Primary Focus |
|---|---:|---|---|
| Response Evaluation | 10 | Markdown + CSV | AI response evaluation |
| Data Quality | 10 | Markdown + CSV | Structured data quality evaluation |

---

## Future Extensions

Possible future additions include:

- Structured CSV datasets
- JSON annotation format
- Multi-dimensional evaluation records
- Pairwise evaluation datasets
- Inter-annotator agreement examples
- Quality-control samples
- Error analysis datasets

These extensions can be added as the portfolio develops.
