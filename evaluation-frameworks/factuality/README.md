# Factuality & Accuracy Evaluation 🔎

A practical framework for evaluating whether factual claims in an AI-generated response are accurate, supported by available evidence, and consistent with the information provided in the task.

This framework focuses on **factual correctness and evidential support**, rather than instruction following, writing quality, or general usefulness.

---

## 🎯 Objective

The objective is to determine whether the factual claims made in a response are:

- Accurate
- Consistent with the available evidence
- Appropriately qualified when uncertainty exists
- Free from unsupported factual assertions
- Free from fabricated information

The evaluation should focus on claims that can reasonably be assessed from the available evidence.

---

## 🔄 Evaluation Workflow

**Understand the Task → Identify Factual Claims → Determine Verification Requirements → Check Available Evidence → Compare Claims → Identify Errors → Assess Severity → Determine Judgment → Write Rationale**

---

## 1. Understand the Task Context

Before evaluating factuality, understand:

- The user's question
- The information provided in the task
- Any supplied reference material
- The time context
- The scope of the requested answer

The same statement may require different evaluation depending on the information available in the task.

---

## 2. Identify Factual Claims

Break the response into individual factual claims that can be evaluated.

Examples include:

- Dates
- Names
- Numbers
- Locations
- Definitions
- Historical events
- Scientific statements
- Product specifications
- Relationships between entities
- Cause-and-effect claims

Do not treat opinions, preferences, or clearly marked hypothetical statements as factual claims unless the task requires them to be evaluated as such.

---

## 3. Determine Verification Requirements

For each factual claim, determine whether verification is required.

Consider:

- Is the claim objectively verifiable?
- Is supporting evidence available?
- Is the claim dependent on current information?
- Does the task provide reference material?
- Does the response present uncertainty appropriately?

Claims that cannot reasonably be verified from the available evidence should not automatically be classified as false.

---

## 4. Compare Claims Against Evidence

Compare the response directly with the available evidence.

A useful structure is:

| Claim | Available Evidence | Assessment |
|---|---|---|
| Claim A | Evidence supports the statement | Supported |
| Claim B | Evidence contradicts the statement | Incorrect |
| Claim C | No sufficient evidence available | Unsupported / Unverified |

Focus on the relationship between the claim and the evidence.

---

## 5. Classify Factual Issues

Common factual issues include:

### Incorrect Fact

The response makes a claim that contradicts reliable available evidence.

### Unsupported Claim

The response presents a factual assertion without sufficient evidence when evidence is required.

### Fabricated Information

The response invents a fact, source, statistic, event, quotation, or other information that is not supported by the available evidence.

### Misleading Statement

The individual statement may contain some correct information but creates a materially misleading impression through omission, framing, or inaccurate interpretation.

### Outdated Information

The claim may have been accurate previously but is no longer accurate for the relevant time period.

### Internal Contradiction

Different parts of the response make incompatible factual claims.

---

## 6. Assess Error Severity

Not all factual errors have the same impact.

### Critical

An error that fundamentally changes the answer or could lead to serious consequences.

### Major

An error that materially affects the correctness or usefulness of the response.

### Minor

A small factual error that does not materially change the main answer.

Severity should be determined according to the task context and the impact of the error.

---

## 7. Distinguish Fact From Uncertainty

A response should not be penalized simply for acknowledging uncertainty when uncertainty is appropriate.

Evaluate whether the response:

- Clearly distinguishes known facts from uncertainty
- Avoids presenting speculation as fact
- Uses appropriate qualifications
- Does not claim unsupported certainty

Appropriate uncertainty can be preferable to an unsupported definitive statement.

---

## 8. Check Numerical Claims

Numbers require particular attention because small errors can materially change meaning.

Review:

- Dates
- Percentages
- Quantities
- Measurements
- Financial figures
- Statistics
- Calculations

Check whether:

- The number matches the available evidence
- Units are correct
- Calculations are internally consistent
- Comparisons use the correct baseline

---

## 9. Check Sources and Attributions

When a response references sources, evaluate whether the attribution is supported.

Review:

- Source names
- Report titles
- Publication dates
- Quoted statements
- Claimed findings
- Links or references where available

Do not assume that mentioning a source automatically makes a claim factual.

---

## 10. Determine the Overall Judgment

After evaluating individual claims, determine the overall factuality level according to the applicable rubric.

A practical scale is:

### Accurate

The response's meaningful factual claims are supported and no material factual errors are identified.

### Mostly Accurate

The response is substantially correct but contains one or more limited factual issues that do not materially change the main answer.

### Inaccurate

The response contains one or more material factual errors that significantly affect the answer.

The exact judgment should depend on the evaluation task and applicable rubric.

---

## 🧪 Example

### User Task

> According to the information provided, which city is the capital of Country A?

### Reference Information

> The capital of Country A is City X.

### AI Response

> The capital of Country A is City Y.

### Evaluation

| Element | Assessment |
|---|---|
| Factual claim | Country A's capital is City Y |
| Available evidence | Country A's capital is City X |
| Issue | Contradiction |
| Severity | Major |
| Overall judgment | Inaccurate |

### Rationale

The response identifies City Y as the capital, but the provided reference information explicitly identifies City X. The factual claim therefore contradicts the available evidence.

---

## 🔍 Edge Cases

### Missing Evidence

If sufficient evidence is unavailable, distinguish **unverified** from **false**.

### Ambiguous Claims

If a statement has multiple reasonable interpretations, evaluate the interpretation supported by the task context before assigning an error.

### Time-Sensitive Claims

Consider the relevant date or time period when evaluating claims that can change over time.

### Estimates

An estimate should not automatically be treated as an exact factual claim if the response clearly identifies it as an estimate.

### Opinions

Clearly identified opinions should not be evaluated as factual errors unless they contain factual claims that can independently be assessed.

---

## 📊 Quality Assurance Checklist

Before finalizing an evaluation:

- [ ] I identified the relevant factual claims
- [ ] I understood the task context
- [ ] I identified the available evidence
- [ ] I compared claims directly against evidence
- [ ] I distinguished unsupported claims from demonstrably false claims
- [ ] I considered the relevant time period
- [ ] I checked important numbers and dates
- [ ] I assessed the severity of identified errors
- [ ] The overall judgment is consistent with the evidence
- [ ] The rationale identifies the specific factual issue

---

## 📝 Evaluation Record Structure

### Task

What question or task was given?

### Evidence

What reference information is available?

### Claims

Which factual claims does the response make?

### Claim Assessment

| Claim | Evidence | Status | Severity |
|---|---|---|---|
| Claim 1 | Supporting evidence | Supported | — |
| Claim 2 | Contradicting evidence | Incorrect | Major |
| Claim 3 | No sufficient evidence | Unverified | — |

### Overall Judgment

**Accurate / Mostly Accurate / Inaccurate**

### Rationale

Explain the most important factual findings using specific evidence.

---

## 📌 Key Principles

1. **Evaluate factual claims against available evidence.**
2. **Separate unsupported claims from demonstrably false claims.**
3. **Consider the relevant time period and task context.**
4. **Do not treat uncertainty as factual error when uncertainty is appropriate.**
5. **Check important numbers, dates, and attributions carefully.**
6. **Assess the severity and impact of factual errors.**
7. **Use specific evidence to support factuality judgments.**
8. **Do not confuse factuality with instruction following or writing quality.**

---

## 🔗 Related Portfolio Sections

- [AI Evaluation & Data Quality Portfolio](../../README.md)
- [Instruction Following Framework](../instruction-following/)

---

## 🔐 Documentation Scope

This framework documents a general methodology for evaluating factual accuracy.

Practical examples using this framework are documented separately in the `evaluation-examples/` section.

No private evaluation tasks, proprietary datasets, platform credentials, or confidential work materials are included.
