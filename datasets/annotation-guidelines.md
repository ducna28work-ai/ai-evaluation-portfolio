# Annotation Guidelines

These guidelines define a structured process for annotating synthetic AI evaluation records.

The purpose is to support consistent, evidence-based, and reproducible evaluation decisions.

All examples in these guidelines are synthetic.

---

## 1. Annotation Workflow

Annotators should follow the same sequence for each evaluation record:

**Understand the Task → Identify Requirements → Apply Criteria → Review Evidence → Assign Judgment → Write Rationale → Perform QA**

Do not assign a judgment before identifying the relevant evidence.

---

# 2. Understand the Task

Before evaluating a response, identify:

- What the user requested
- Required output format
- Required quantity
- Language requirements
- Scope constraints
- Special conditions
- Reference information, when provided

### Example

User request:

> Give three benefits of internal linking and one example for each.

Required components:

- Three benefits
- One example for each benefit
- Topic: internal linking

A response containing only two benefits should not be considered fully compliant.

---

# 3. Identify the Evaluation Dimension

Select the dimension that best matches the issue being evaluated.

Available dimensions:

- Instruction Following
- Factuality & Accuracy
- Relevance
- Completeness
- Response Quality
- Safety & Policy Compliance

Do not combine unrelated dimensions when the task requires a specific evaluation criterion.

---

# 4. Instruction Following

Evaluate whether the response satisfies the explicit requirements of the task.

Check:

- Quantity
- Format
- Language
- Scope
- Requested structure
- Explicit constraints

### Example

Requirement:

> Give exactly three reasons.

Response:

> Gives two reasons.

Judgment:

**Partially Compliant**

Reason:

The response does not satisfy the required quantity.

---

# 5. Factuality & Accuracy

Evaluate factual claims against the available evidence.

Use the following process:

1. Identify the factual claim.
2. Identify the available reference or evidence.
3. Compare the claim with the evidence.
4. Determine whether the claim is supported, contradicted, or cannot be verified.
5. Record the relevant evidence.

### Possible Judgments

- Accurate
- Mostly Accurate
- Inaccurate

Do not treat an unsupported claim as automatically false when the available evidence is insufficient to verify it.

---

# 6. Relevance

Determine whether the response addresses the user's actual request.

Check:

- Topical alignment
- Directness
- Scope
- Unnecessary tangents
- Useful versus irrelevant context

Additional information is not automatically irrelevant.

The key question is whether the additional content helps answer the user's request or unnecessarily moves outside the requested scope.

### Example

A response gives the requested three SEO benefits and then adds a long explanation of unrelated SEO topics.

Possible judgment:

**Mostly Relevant**

Reason:

The requested information is present, but additional content reduces scope control.

---

# 7. Completeness

Determine whether all important requested components are present.

Check:

- Every requested item
- Required examples
- Required explanations
- Multi-part requirements
- Quantitative requirements

### Example

Task:

> Give three benefits and one example for each.

Response:

- Three benefits
- Two examples

Judgment:

**Mostly Complete**

Reason:

The primary concepts are present, but one required example is missing.

---

# 8. Response Quality

Evaluate the quality of the response as a communication artifact.

Consider:

- Clarity
- Organization
- Coherence
- Usefulness
- Appropriate detail
- Concision
- Readability
- Tone
- Actionability

Do not use response quality as a substitute for factuality.

A response can be:

- Well written but factually incorrect
- Factually accurate but poorly organized
- Complete but unnecessarily verbose

These dimensions should be evaluated separately when required.

---

# 9. Safety & Policy Compliance

Evaluate whether the response provides an appropriate level of assistance.

Check:

- Nature of the request
- Potential risk
- Operational detail
- Whether the response enables harmful activity
- Whether a safe alternative is appropriate
- Whether sensitive information is exposed

General defensive information should not automatically be treated as unsafe.

The evaluation should focus on the actual level of assistance provided.

---

# 10. Evidence

Every non-trivial judgment should be supported by observable evidence.

Good evidence:

> The user requested three reasons, but the response contains only two.

Weak evidence:

> The response is not very good.

Evidence should identify the specific feature of the response that supports the judgment.

---

# 11. Severity

Use severity when the evaluation framework requires it.

### Minor

Limited impact that does not substantially prevent the response or record from being useful.

Examples:

- Small formatting inconsistency
- Minor scope expansion
- Clear normalization issue

### Major

An issue that meaningfully affects task completion or data reliability.

Examples:

- Missing required component
- Incorrect factual claim
- Invalid required value
- Confirmed duplicate

### Critical

An issue that substantially prevents safe or reliable use.

Examples:

- Severe structural failure
- Systematic annotation failure
- Serious safety violation

Severity should reflect impact, not personal preference.

---

# 12. Writing the Rationale

A good rationale should explain:

**What happened → Why it matters → How the evidence supports the judgment**

### Example

Weak:

> The answer is incomplete.

Better:

> The task requires three benefits and one example for each. The response provides all three benefits but gives examples for only two, so one required component is missing.

The rationale should be concise and directly connected to the evidence.

---

# 13. Handling Ambiguity

When the evidence does not support a confident decision:

- Record the uncertainty
- Avoid inventing information
- Avoid assuming user intent without evidence
- Escalate when appropriate

### Example

If a required field is missing and multiple possible values could be correct:

**Do not guess.**

Record the missing value and escalate for review.

---

# 14. Avoiding Double Counting

Do not automatically classify the same problem as multiple unrelated errors.

Example:

A response gives two reasons instead of three.

Primary issue:

**Instruction Following**

It may also affect completeness depending on the evaluation framework, but the evaluator should follow the specific dimension and criteria being assessed rather than assigning multiple labels without justification.

---

# 15. Pairwise Comparison

When comparing two responses:

1. Confirm both responses address the same task.
2. Apply the same evaluation criteria.
3. Review each response independently.
4. Identify evidence for each.
5. Compare the dimension-level findings.
6. Record the comparative judgment.
7. Allow a tie when the evidence does not establish a meaningful difference.

Do not choose a response simply because it sounds better.

---

# 16. Data Quality Annotation

For structured data, check:

- Completeness
- Validity
- Consistency
- Uniqueness
- Format compliance
- Annotation consistency

Follow this sequence:

**Detect → Classify → Validate → Correct or Escalate → QA**

### Example

Observed:

`billing`

Expected:

`Billing`

If the intended value is unambiguous:

**Decision: Normalize**

---

### Missing Value

Observed:

`Priority = empty`

If the correct priority cannot be determined:

**Decision: Escalate**

Do not invent a replacement.

---

### Duplicate

If the same record appears twice:

1. Identify the potential duplicate.
2. Compare relevant fields.
3. Confirm duplication.
4. Review removal or merge.
5. Document the decision.

---

# 17. Quality Assurance

Before finalizing an annotation:

### Task Understanding

- [ ] User requirements identified
- [ ] Constraints identified
- [ ] Required quantity identified
- [ ] Required format identified

### Evaluation

- [ ] Correct dimension selected
- [ ] Relevant evidence identified
- [ ] Judgment supported by evidence
- [ ] Severity assigned consistently
- [ ] Rationale explains the decision

### Data Quality

- [ ] Required fields checked
- [ ] Validity rules checked
- [ ] Consistency checked
- [ ] Duplicates checked
- [ ] Ambiguous values escalated

### Final QA

- [ ] No unsupported assumptions
- [ ] No invented information
- [ ] Terminology is consistent
- [ ] Annotation follows the defined rubric
- [ ] Final judgment matches the evidence

---

# 18. Annotation Record

Use this structure for a standard evaluation:

| Field | Description |
|---|---|
| Task ID | Evaluation identifier |
| User Prompt | Task being evaluated |
| AI Response | Response being reviewed |
| Dimension | Evaluation criterion |
| Evidence | Observable supporting evidence |
| Judgment | Evaluation result |
| Severity | Impact level when applicable |
| Rationale | Explanation of the judgment |
| QA Status | Final quality-control status |

For data quality tasks:

| Field | Description |
|---|---|
| Record ID | Dataset record identifier |
| Field | Affected field |
| Observed Value | Value found |
| Expected Standard | Applicable rule |
| Issue Type | Quality issue |
| Severity | Impact level |
| Decision | Action taken |
| Evidence | Supporting evidence |
| Rationale | Explanation |
| QA Status | Final status |

---

# 19. Core Annotation Principles

### Evidence Before Judgment

Identify evidence before assigning a label.

### Requirements Before Evaluation

Understand what the task requires before judging the response.

### Consistent Criteria

Apply the same criteria to comparable cases.

### Separate Dimensions

Do not treat every quality problem as the same type of issue.

### No Unsupported Assumptions

Do not invent missing information or infer unsupported intent.

### Explicit Rationale

Every important judgment should be explainable.

### QA Before Finalization

Review annotations before considering them complete.

---

## Summary

The annotation process can be summarized as:

**Understand → Identify → Evaluate → Evidence → Judge → Explain → QA**

The objective is not simply to assign labels.

The objective is to produce **consistent, evidence-based, reproducible evaluation decisions**.
