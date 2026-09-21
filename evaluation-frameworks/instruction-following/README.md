# Instruction Following Evaluation 📋

A practical framework for evaluating whether an AI-generated response correctly follows the user's instructions, constraints, requested format, and task requirements.

This framework focuses on **instruction compliance** rather than whether the response is simply well-written or factually correct.

---

## 🎯 Objective

The objective is to determine whether a response successfully fulfills the requirements specified by the user.

An evaluation should distinguish between:

- What the user explicitly requested
- What constraints were specified
- What the response actually delivered
- Which requirements were satisfied
- Which requirements were missed or violated

The evaluation should be based on observable evidence in the response.

---

## 🔄 Evaluation Workflow

**Understand the Task → Extract Requirements → Identify Constraints → Review Response → Map Evidence → Assess Compliance → Determine Judgment → Write Rationale**

---

## 1. Understand the Task

Read the complete user instruction before evaluating the response.

Identify:

- The main task
- The expected outcome
- Required information
- Required format
- Explicit constraints
- Quantity requirements
- Language requirements
- Style requirements
- Other task-specific conditions

Do not evaluate individual sentences before understanding the complete task.

---

## 2. Extract Explicit Requirements

Convert the user's request into a structured checklist.

For example:

| Requirement | Type |
|---|---|
| Answer the user's question | Core task |
| Provide 3 examples | Quantity |
| Use Vietnamese | Language |
| Keep the response concise | Style |
| Use a table | Format |
| Do not include unrelated information | Constraint |

The checklist should contain requirements that can be evaluated from the response.

---

## 3. Identify Constraints

Separate positive requirements from restrictions.

Common constraints include:

- Word or character limits
- Number of items
- Required format
- Language
- Tone
- Prohibited content
- Required sources
- Specific output structure
- Scope limitations

A response can be factually correct but still fail instruction-following if it violates an important explicit constraint.

---

## 4. Review the Response

Evaluate the response against the extracted requirements.

For each requirement, determine whether the response:

- Satisfies it
- Partially satisfies it
- Fails to satisfy it
- Violates it

Focus on what is actually present in the response rather than what the model may have intended.

---

## 5. Map Evidence

Record concrete evidence supporting the evaluation.

A useful structure is:

| Requirement | Response Evidence | Assessment |
|---|---|---|
| Required language | Response is written in Vietnamese | Satisfied |
| Three examples | Only two examples provided | Not satisfied |
| Concise format | Response contains unnecessary sections | Partially satisfied |

Evidence should be specific enough for another evaluator to understand the judgment.

---

## 6. Assess Requirement Importance

Not every missed instruction has the same significance.

Classify requirements as:

### Critical

A requirement directly related to the core task or an explicit hard constraint.

### Important

A requirement that materially affects usefulness or compliance but does not completely define the task.

### Minor

A preference or secondary requirement where deviation has limited impact.

This distinction helps prevent minor issues from being treated the same as major instruction failures.

---

## 7. Determine the Overall Judgment

After reviewing individual requirements, determine the overall level of instruction compliance.

A practical judgment scale is:

### Fully Compliant

The response satisfies the important requirements and does not violate meaningful constraints.

### Partially Compliant

The response fulfills the main task but misses or violates one or more meaningful requirements.

### Not Compliant

The response fails to fulfill the core task or violates a critical instruction.

The judgment should follow the defined evaluation rubric rather than personal preference.

---

## 8. Write the Evaluation Rationale

A strong rationale should explain:

1. What the task required
2. What the response provided
3. Which requirements were satisfied or missed
4. Why those differences affect the judgment

A useful rationale is:

**Requirement → Evidence → Impact → Judgment**

Avoid vague explanations such as:

- "The answer is bad."
- "It doesn't follow instructions."
- "This feels incomplete."

Instead, identify the specific requirement and the observable evidence.

---

## 9. Common Instruction-Following Errors

Common failure patterns include:

### Missing Requirements

The response ignores one or more explicit requirements.

### Format Violation

The response provides the requested information but uses the wrong format.

### Quantity Error

The response provides too many or too few requested items.

### Constraint Violation

The response violates an explicit restriction.

### Partial Completion

The response addresses only part of the requested task.

### Scope Expansion

The response introduces unnecessary content outside the requested scope.

### Language or Style Mismatch

The response uses a different language, tone, or style from the explicit requirement.

### Conflicting Instructions

The response follows one instruction while violating another instruction with equal or higher priority.

---

## 🧪 Example Evaluation

### User Task

> Give me three short reasons why exercise is beneficial. Answer in Vietnamese.

### AI Response

> Tập thể dục giúp cải thiện sức khỏe tim mạch và tăng sức bền. Nó cũng có thể giúp giảm căng thẳng.

### Evaluation

| Requirement | Evidence | Assessment |
|---|---|---|
| Provide three reasons | Only two reasons are provided | Not satisfied |
| Answer in Vietnamese | Response is written in Vietnamese | Satisfied |
| Keep reasons short | Both reasons are concise | Satisfied |

### Overall Judgment

**Partially Compliant**

### Rationale

The response follows the language and concise-format requirements but provides only two reasons instead of the requested three. The missing third reason prevents full compliance with the task.

---

## 🔍 Edge Cases

Some evaluations require additional judgment.

### Implicit vs. Explicit Requirements

Do not treat an unstated personal preference as an explicit instruction.

For example, if a user asks for "three examples," the number three is explicit.

If the user does not specify the preferred order of the examples, do not mark the response incorrect solely because it uses a different order.

### Multiple Instructions

When a task contains several requirements, evaluate each requirement separately before determining the overall judgment.

### Ambiguous Instructions

If an instruction is genuinely ambiguous, avoid inventing a strict interpretation that the user did not specify.

### Conflicting Requirements

When instructions conflict, identify the conflict and determine which instruction should take precedence according to the applicable evaluation rules.

---

## 📊 Quality Assurance Checklist

Before finalizing an evaluation:

- [ ] I identified the core task
- [ ] I extracted explicit requirements
- [ ] I identified relevant constraints
- [ ] I evaluated each important requirement
- [ ] I used observable response evidence
- [ ] I distinguished major and minor issues
- [ ] I did not rely on personal preference
- [ ] The overall judgment is consistent with the evidence
- [ ] The rationale clearly explains the judgment

---

## 🛠️ Evaluation Record Structure

A structured evaluation can use the following format:

**Task**

What did the user ask for?

**Requirements**

What explicit requirements must the response satisfy?

**Evidence**

What does the response actually contain?

**Assessment**

Which requirements are satisfied, partially satisfied, or not satisfied?

**Judgment**

What is the overall compliance level?

**Rationale**

What evidence supports the judgment?

---

## 📌 Key Principles

1. **Evaluate against the user's instructions, not personal preference.**
2. **Extract requirements before judging the response.**
3. **Use observable evidence to support evaluation decisions.**
4. **Distinguish critical requirements from minor preferences.**
5. **Evaluate each requirement before determining the overall judgment.**
6. **Do not confuse factual accuracy with instruction following.**
7. **Do not infer unstated requirements without sufficient evidence.**
8. **Keep the rationale concise, specific, and evidence-based.**

---

## 🔗 Related Portfolio Sections

- [AI Evaluation & Data Quality Portfolio](../../README.md)

---

## 🔐 Documentation Scope

This framework documents a general methodology for evaluating instruction following.

Practical evaluation examples using this framework are documented separately in the `evaluation-examples/` section.

No private evaluation tasks, proprietary datasets, platform credentials, or confidential work materials are included.
