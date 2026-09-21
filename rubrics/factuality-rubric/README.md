# Factuality & Accuracy Rubric 🔎

A structured rubric for evaluating whether factual claims in an AI-generated response are accurate, supported by available evidence, and appropriately qualified when uncertainty exists.

This rubric is designed to support consistent and evidence-based factuality evaluation.

---

## 🎯 Evaluation Objective

The rubric evaluates whether a response:

- Makes factually accurate claims
- Aligns factual claims with available evidence
- Avoids unsupported factual assertions
- Avoids fabricated information
- Represents uncertainty appropriately
- Maintains factual consistency throughout the response

---

## 📊 Evaluation Scale

| Rating | Definition |
|---|---|
| **Accurate** | Meaningful factual claims are supported by available evidence and no material factual errors are identified. |
| **Mostly Accurate** | The response is substantially correct but contains one or more limited factual issues that do not materially change the main answer. |
| **Inaccurate** | The response contains one or more material factual errors that significantly affect the answer. |

The applicable evaluation task may define a different scale. When a task-specific rubric exists, that rubric takes precedence.

---

## 1. Identify Factual Claims

Before assigning a rating, identify claims that can be evaluated as facts.

Potential claim types include:

- Dates
- Names
- Numbers
- Locations
- Definitions
- Historical events
- Scientific statements
- Product specifications
- Statistics
- Relationships between entities
- Cause-and-effect claims

Clearly identified opinions, preferences, and hypothetical statements should not automatically be treated as factual claims.

---

## 2. Identify Available Evidence

Determine what evidence is available for evaluating the claims.

Evidence may include:

- Information provided directly in the task
- Reference documents
- Structured data
- Authoritative sources where the task permits external verification
- Explicit information contained elsewhere in the response

The evaluation should clearly distinguish between **available evidence** and information that has not been verified.

---

## 3. Claim-Level Assessment

Evaluate each meaningful factual claim independently.

| Status | Definition |
|---|---|
| **Supported** | The available evidence supports the claim. |
| **Contradicted** | The available evidence directly conflicts with the claim. |
| **Unsupported** | There is insufficient evidence to establish the claim as correct. |
| **Partially Supported** | The claim contains both supported and unsupported or incorrect elements. |
| **Not Verifiable** | The claim cannot reasonably be assessed with the available information. |

An unsupported claim should not automatically be classified as false without sufficient evidence.

---

## 4. Error Categories

### Incorrect Fact

The response makes a factual statement that contradicts reliable available evidence.

### Unsupported Claim

The response presents a factual assertion for which sufficient supporting evidence is unavailable.

### Fabricated Information

The response invents information such as:

- Statistics
- Events
- Sources
- Quotations
- Names
- References
- Product details

without supporting evidence.

### Misleading Statement

The response presents information in a way that creates a materially inaccurate impression despite containing some individually correct information.

### Outdated Information

The response provides information that may have been accurate previously but is incorrect for the relevant time period.

### Internal Contradiction

Different parts of the response make incompatible factual claims.

---

## 5. Error Severity

Assess the impact of factual errors within the context of the task.

### Critical

The error fundamentally changes the answer or could create serious consequences.

### Major

The error materially affects the correctness, interpretation, or usefulness of the response.

### Minor

The error has limited impact and does not materially change the main answer.

Severity should be based on the task context rather than the evaluator's personal preference.

---

## 6. Overall Judgment Rules

### Accurate

Use when:

- Meaningful factual claims are supported
- No material factual contradictions are identified
- Any uncertainty is appropriately represented
- Minor issues, if present, do not materially affect the answer

### Mostly Accurate

Use when:

- The main factual content is correct
- One or more limited issues are present
- The issues do not materially change the main answer

### Inaccurate

Use when:

- A material factual claim is contradicted by reliable evidence
- A critical factual error changes the answer
- Significant fabricated information affects the response
- Multiple major factual errors materially reduce correctness

---

## 7. Uncertainty & Verification

Evaluators should distinguish between:

**False → Evidence contradicts the claim**

and

**Unverified → Evidence is insufficient to establish whether the claim is true**

A response should not be penalized merely because it acknowledges uncertainty where uncertainty is appropriate.

Evaluate whether the response:

- Distinguishes facts from uncertainty
- Avoids unsupported certainty
- Uses appropriate qualifications
- Clearly indicates when information cannot be verified

---

## 8. Time-Sensitive Claims

Some facts depend on a specific time period.

When evaluating such claims, consider:

- The date of the task
- The relevant comparison period
- Whether the information can change over time
- Whether the response specifies a relevant date

A statement that was historically correct may still be inaccurate if the task asks about the current situation.

---

## 9. Numerical & Quantitative Claims

Pay particular attention to:

- Percentages
- Dates
- Quantities
- Measurements
- Financial figures
- Statistics
- Calculations

Check:

- Numerical accuracy
- Units
- Baselines
- Comparisons
- Internal consistency

A small numerical error may be minor or major depending on its effect on the answer.

---

## 10. Sources & Attributions

When the response references external sources, evaluate whether the attribution is supported.

Review:

- Source identity
- Publication or report title
- Date
- Quoted information
- Claimed findings
- Attribution accuracy

Mentioning a source does not by itself establish that a factual claim is correct.

---

## 🧪 Evaluation Record Template

### Task

What question or task was given?

### Evidence

What reference information or verification sources are available?

### Claims

What factual claims does the response make?

### Claim Assessment

| Claim | Evidence | Status | Severity |
|---|---|---|---|
| Claim 1 | Supporting evidence | Supported | — |
| Claim 2 | Contradicting evidence | Contradicted | Major |
| Claim 3 | Insufficient evidence | Unsupported | — |

### Overall Judgment

**Accurate / Mostly Accurate / Inaccurate**

### Rationale

Explain the most important factual findings and cite the evidence used for the judgment where applicable.

---

## 🔍 Common Evaluation Errors

Evaluators should avoid:

### Plausibility Bias

Do not classify a claim as accurate merely because it sounds reasonable.

### Unsupported Certainty

Do not treat a confident tone as evidence of factual correctness.

### False Equivalence

Do not treat "not verified" as automatically equivalent to "false."

### Ignoring Time Context

Do not evaluate time-sensitive claims without considering the relevant period.

### Source Assumption

Do not assume a claim is accurate simply because the response names a source.

### Personal Knowledge Bias

Do not replace the defined evidence standard with personal assumptions or memory.

---

## 📊 Quality Assurance Checklist

Before finalizing an evaluation:

- [ ] I identified the relevant factual claims
- [ ] I understood the task context
- [ ] I identified the available evidence
- [ ] I compared claims against evidence
- [ ] I distinguished unsupported claims from contradicted claims
- [ ] I considered the relevant time period
- [ ] I checked important numerical claims
- [ ] I considered source attribution where relevant
- [ ] I assessed error severity
- [ ] The overall judgment follows the evidence
- [ ] The rationale identifies the key factual issue

---

## 📌 Key Principles

1. **Evaluate factual claims against available evidence.**
2. **Separate unsupported claims from demonstrably false claims.**
3. **Consider time and task context.**
4. **Do not treat appropriate uncertainty as an error.**
5. **Check important numbers, dates, and attributions carefully.**
6. **Assess factual errors according to their impact.**
7. **Use specific evidence to support judgments.**
8. **Do not confuse factuality with instruction following or writing quality.**

---

## 🔗 Related Portfolio Sections

- [Factuality & Accuracy Framework](../../evaluation-frameworks/factuality/)
- [Factuality & Accuracy Evaluation Example](../../evaluation-examples/factuality/)
- [Instruction Following Rubric](../instruction-following-rubric/)
- [AI Evaluation & Data Quality Portfolio](../../README.md)

---

## 🔐 Documentation Scope

This rubric documents a general methodology for evaluating factual accuracy.

It does not contain private platform guidelines, proprietary evaluation instructions, confidential benchmark data, or private work materials.
