# Instruction Following Rubric 📋

A structured rubric for evaluating whether an AI-generated response follows the explicit requirements and constraints of a user task.

This rubric is designed to support consistent and evidence-based instruction-following evaluation.

---

## 🎯 Evaluation Objective

The rubric evaluates whether a response:

- Completes the requested task
- Follows explicit instructions
- Respects stated constraints
- Uses the requested format
- Provides the requested quantity
- Uses the requested language or style
- Avoids meaningful instruction violations

The rubric should be applied to the task requirements rather than personal preference.

---

## 📊 Evaluation Scale

| Rating | Definition |
|---|---|
| **Fully Compliant** | The response satisfies all important explicit requirements and does not violate meaningful constraints. |
| **Partially Compliant** | The response fulfills the main task but misses or violates one or more meaningful requirements. |
| **Not Compliant** | The response fails to fulfill the core task or violates a critical instruction. |

---

## 1. Requirement Identification

Before assigning a rating, identify the explicit requirements in the user task.

Consider:

- Core task
- Required information
- Required quantity
- Required language
- Required format
- Length constraints
- Style requirements
- Explicit restrictions
- Other task-specific conditions

Do not create requirements that the user did not specify.

---

## 2. Requirement-Level Assessment

Evaluate each requirement independently.

| Requirement Status | Meaning |
|---|---|
| **Satisfied** | The response clearly fulfills the requirement. |
| **Partially Satisfied** | The response addresses the requirement but does not fully satisfy it. |
| **Not Satisfied** | The response does not fulfill the requirement. |
| **Violated** | The response directly conflicts with an explicit constraint. |
| **Not Applicable** | The requirement does not apply to the response being evaluated. |

---

## 3. Requirement Importance

Not every requirement has the same impact on the final judgment.

### Critical Requirement

A requirement that defines the core task or represents a hard constraint.

Examples:

- Required output type
- Essential requested information
- Explicit safety restriction
- Mandatory format when central to the task

Failure to satisfy a critical requirement may result in a **Not Compliant** judgment.

### Important Requirement

A requirement that materially affects the usefulness or completeness of the response.

Failure may contribute to a **Partially Compliant** judgment.

### Minor Requirement

A secondary preference or detail with limited impact on task completion.

A minor deviation should not automatically cause the response to fail overall.

---

## 4. Evidence Standard

Every meaningful evaluation judgment should be supported by observable evidence.

Evidence may include:

- Missing requested information
- Incorrect number of items
- Wrong language
- Incorrect format
- Unrequested content
- Explicitly prohibited content
- Partial completion
- Direct contradiction of the task requirements

Avoid relying on assumptions about the model's intention.

---

## 5. Overall Judgment Rules

### Fully Compliant

Use when:

- Core requirements are satisfied
- Important requirements are satisfied
- No meaningful constraints are violated
- Minor deviations do not materially affect task completion

### Partially Compliant

Use when:

- The core task is substantially addressed
- One or more meaningful requirements are missed
- The response remains partially useful
- No critical failure prevents the task from being completed

### Not Compliant

Use when:

- The core task is not fulfilled
- A critical requirement is missed
- A critical constraint is violated
- The response is fundamentally incompatible with the requested task

---

## 6. Example Decision Logic

### Scenario A — Fully Compliant

User requests:

> Give me three short examples in Vietnamese.

Response provides:

- Three examples
- Vietnamese language
- Concise format

**Judgment: Fully Compliant**

---

### Scenario B — Partially Compliant

User requests:

> Give me three short examples in Vietnamese.

Response provides:

- Two examples
- Vietnamese language
- Concise format

**Judgment: Partially Compliant**

The core task is addressed, but the explicit quantity requirement is not fully satisfied.

---

### Scenario C — Not Compliant

User requests:

> Give me three short examples in Vietnamese.

Response provides:

> Here are five examples in English.

**Judgment: Not Compliant**

The response fails multiple explicit requirements, including language and quantity, and does not sufficiently follow the requested task.

---

## 🔍 Common Evaluation Errors

Evaluators should avoid:

### Personal Preference

Do not mark a response as incorrect simply because you would have written it differently.

### Unstated Requirements

Do not assume that an unstated preference is an instruction.

### Overweighting Minor Issues

Do not treat small stylistic differences as equivalent to missing core requirements.

### Ignoring Explicit Constraints

Do not overlook clear requirements simply because the response is otherwise well-written.

### Unsupported Judgment

Do not assign an overall rating without identifying the evidence supporting it.

---

## 🧪 Evaluation Record Template

Use the following structure when applying this rubric:

### Task

Describe the user's request.

### Requirements

List the explicit requirements.

### Requirement Assessment

| Requirement | Importance | Evidence | Status |
|---|---|---|---|
| Requirement 1 | Critical | Response evidence | Satisfied |
| Requirement 2 | Important | Response evidence | Partially Satisfied |
| Requirement 3 | Minor | Response evidence | Satisfied |

### Overall Judgment

**Fully Compliant / Partially Compliant / Not Compliant**

### Rationale

Explain the judgment using the most important evidence.

---

## 📌 Key Principles

1. **Evaluate explicit requirements before overall quality.**
2. **Use observable evidence for meaningful judgments.**
3. **Separate requirement-level assessment from the overall rating.**
4. **Give greater weight to critical requirements.**
5. **Do not invent requirements that the user did not specify.**
6. **Do not confuse writing quality with instruction compliance.**
7. **Keep judgments consistent with the evidence.**
8. **Make the rationale clear enough for another evaluator to reproduce the decision.**

---

## 🔗 Related Portfolio Sections

- [Instruction Following Framework](../../evaluation-frameworks/instruction-following/)
- [Instruction Following Evaluation Example](../../evaluation-examples/instruction-following/)
- [AI Evaluation & Data Quality Portfolio](../../README.md)

---

## 🔐 Documentation Scope

This rubric is a general evaluation framework created for portfolio demonstration.

It does not contain private platform guidelines, proprietary evaluation instructions, confidential benchmark data, or private work materials.
