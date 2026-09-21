# Completeness Evaluation Framework

## Overview

Completeness evaluation assesses whether an AI response provides all important information required to fulfill the user's request.

A complete response should address the major requirements of the task without leaving important requested elements unanswered.

Completeness is different from relevance, factuality, and instruction following:

- **Completeness:** Does the response cover the important parts of the task?
- **Relevance:** Does the response stay focused on the user's intent?
- **Factuality:** Are the claims accurate?
- **Instruction Following:** Does the response follow the explicit requirements and constraints?

A response can be relevant and factually accurate while still being incomplete if it omits an important part of the user's request.

---

## Evaluation Objective

The evaluator should determine whether the response:

1. Identifies and addresses the major requirements of the task.
2. Covers all important requested components.
3. Provides enough information to fulfill the user's intended outcome.
4. Does not omit critical information.
5. Addresses each part of a multi-part request.
6. Provides appropriate supporting detail when required.
7. Maintains an appropriate level of completeness for the task.

The evaluation should focus on **what the user requested versus what the response actually provides**.

---

## Evaluation Workflow

**Understand the Task → Identify Requirements → Determine Required Coverage → Review Response → Map Covered Components → Identify Missing Components → Assess Importance → Make Judgment → Record Rationale → Quality Check**

---

## 1. Understand the Task

Before evaluating completeness, determine what the user expects the response to accomplish.

Consider:

- What is the main objective?
- What specific information is requested?
- Are there multiple questions?
- Are there explicit quantities?
- Are there required steps?
- Are examples requested?
- Is a particular format or output required?
- Does the task contain implicit information necessary to fulfill the user's goal?

The evaluator should understand the task before judging whether anything is missing.

---

## 2. Extract Task Requirements

Break the user's request into discrete requirements.

### Example

User request:

> "Explain three benefits of internal linking and give one practical example for each."

Requirements:

1. Explain benefit one.
2. Explain benefit two.
3. Explain benefit three.
4. Provide an example for benefit one.
5. Provide an example for benefit two.
6. Provide an example for benefit three.

Each requirement should be tracked separately during evaluation.

---

## 3. Determine Requirement Importance

Not every missing detail has the same impact.

Classify requirements as:

### Critical

Missing the requirement prevents the response from fulfilling the main purpose of the task.

### Important

Missing the requirement leaves a meaningful gap but does not completely prevent the user from obtaining value.

### Minor

Missing the requirement has limited impact on the usefulness of the response.

Importance should be determined from the task itself rather than from the amount of text dedicated to a requirement.

---

## 4. Determine Required Coverage

Before reading the response in detail, establish what a sufficiently complete answer should contain.

Required coverage may include:

- Main question
- Sub-questions
- Requested number of items
- Requested examples
- Required steps
- Required comparisons
- Required fields
- Important constraints
- Necessary conclusions
- Requested output components

This creates a reference point for identifying omissions.

---

## 5. Review the Response

Read the complete response and map each major section to the requirements identified from the task.

For each requirement, determine whether it is:

- Fully addressed
- Partially addressed
- Not addressed
- Not applicable

Do not assume that a topic is covered merely because related keywords appear in the response.

---

## 6. Requirement Coverage

A useful coverage model is:

| Status | Meaning |
|---|---|
| Fully Addressed | Requirement is adequately answered |
| Partially Addressed | Requirement is addressed but important information is missing |
| Not Addressed | Requirement is missing |
| N/A | Requirement does not apply |

The evaluator should provide evidence for partial or missing requirements.

---

## 7. Identify Missing Components

Look specifically for omissions such as:

- Unanswered questions
- Missing requested items
- Missing examples
- Missing steps
- Missing comparisons
- Missing conclusions
- Missing requested fields
- Missing important qualifications
- Missing necessary context

The evaluator should distinguish between genuinely missing information and information that is simply expressed differently.

---

## 8. Distinguish Completeness from Relevance

A response may be highly relevant but incomplete.

### Example

User:

> "Give me five benefits of internal linking."

Response:

> "Internal linking improves navigation and helps search engines discover pages."

The response is relevant because it discusses internal linking and its benefits.

However, it is incomplete because the user requested five benefits and only two are provided.

Completeness asks:

> **Were the important requested components covered?**

Relevance asks:

> **Does the response focus on the right information?**

---

## 9. Distinguish Completeness from Length

Longer responses are not automatically more complete.

A response can be lengthy but incomplete if it spends substantial space discussing secondary information while omitting requested components.

Likewise, a concise response can be complete when the task itself requires only a short answer.

Evaluate whether the response contains the **necessary information**, not simply how much information it contains.

---

## 10. Multi-Part Requests

Multi-part requests require component-level evaluation.

### Example

User request:

> "Explain GA4, compare it with Universal Analytics, and list three practical use cases."

Required components:

1. Explanation of GA4.
2. Comparison with Universal Analytics.
3. Three practical use cases.

If the response only explains GA4, it is incomplete even if that explanation is accurate and detailed.

The evaluator should identify which components are missing and assess their importance.

---

## 11. Quantitative Requirements

Some tasks specify an exact or minimum number of outputs.

Examples:

- "Give me five examples."
- "List three reasons."
- "Provide ten keywords."
- "Name two alternatives."

Check whether the response satisfies the requested quantity.

### Example

Requested:

> "Give me five examples."

Provided:

> Three examples.

Assessment:

- Quantity requirement: Partially Addressed
- Completeness issue: Missing requested items

The evaluator should not treat three examples as complete simply because the examples provided are relevant.

---

## 12. Procedural Requests

For tasks asking how to perform something, completeness may depend on whether the important steps are present.

Example:

> "Explain how to create a GA4 conversion event."

A complete response should cover the important steps needed to perform the task, rather than only defining what a conversion event is.

The evaluator should consider the intended outcome of the procedure.

---

## 13. Comparison Requests

For comparison tasks, completeness requires coverage of the requested comparison dimensions.

Example:

> "Compare Tool A and Tool B in terms of price, features, and ease of use."

The evaluator should check:

- Price
- Features
- Ease of use

A response that only discusses features is incomplete even if the feature comparison is detailed.

---

## 14. Missing vs. Unnecessary Information

Completeness does not require every possible detail.

The evaluator should not penalize a response for excluding information that:

- Was not requested.
- Is not necessary to fulfill the task.
- Does not materially affect the requested outcome.

The goal is **sufficient coverage**, not exhaustive coverage of the entire subject.

---

## 15. Appropriate Level of Detail

Completeness depends on task complexity and expected depth.

A simple factual question may require only one concise answer.

A complex procedural or analytical request may require multiple components.

Consider:

- User's wording
- Number of requested components
- Task complexity
- Required output
- Explicit constraints
- Intended use of the answer

Avoid applying the same completeness standard to every task.

---

## 16. Overall Judgment

Use the following completeness scale:

### Complete

The response adequately addresses all important requirements of the task.

Characteristics:

- All major requested components are covered.
- Important quantities are satisfied.
- Required examples, steps, or comparisons are included.
- No critical omission remains.
- The response provides enough information to fulfill the user's intended outcome.

### Mostly Complete

The response addresses nearly all important requirements but has a minor omission or limited gap.

Characteristics:

- Main task is fulfilled.
- Most important components are covered.
- A smaller requested detail may be missing.
- The omission has limited impact on the overall usefulness.

### Partially Complete

The response covers some important requirements but leaves meaningful gaps.

Characteristics:

- One or more important components are missing.
- A multi-part request may be only partially addressed.
- Requested quantity may not be fully satisfied.
- The response provides useful information but does not fully fulfill the task.

### Incomplete

The response fails to cover the major requirements of the task.

Characteristics:

- Critical components are missing.
- Most of the requested task remains unanswered.
- The response does not provide enough information to fulfill the user's main objective.

---

## 17. Evidence-Based Evaluation

Completeness judgments should be supported by observable evidence.

### Strong Rationale

> "The user requested three benefits and one example for each. The response provides all three benefits but gives examples for only two, leaving one requested component incomplete."

### Weak Rationale

> "The answer could have more information."

The rationale should identify:

- What was requested.
- What was provided.
- What is missing.
- Why the missing information matters.

---

## 18. Edge Cases

### Concise Requests

Do not require unnecessary detail when the user asks for a simple answer.

### Implicit Requirements

Consider information that is reasonably necessary to fulfill the user's stated goal, but avoid inventing requirements that the user did not request.

### Ambiguous Requests

If the request is genuinely ambiguous, evaluate completeness against the most reasonable interpretation supported by the task.

### Optional Information

Do not classify optional or unrequested information as missing.

### Relevant but Redundant Information

Repeated information does not compensate for a missing requested component.

### Examples

If the user explicitly requests examples, examples are part of the completeness requirement.

If examples are not requested, they are generally optional unless needed to fulfill the task.

---

## 19. Quality Assurance Checklist

Before finalizing a completeness evaluation:

- [ ] Did I identify the user's main objective?
- [ ] Did I break the task into its major requirements?
- [ ] Did I determine which requirements are critical, important, or minor?
- [ ] Did I check every major requirement against the response?
- [ ] Did I check quantitative requirements?
- [ ] Did I check all parts of multi-part requests?
- [ ] Did I distinguish missing information from optional information?
- [ ] Did I avoid equating response length with completeness?
- [ ] Did I identify specific missing components?
- [ ] Did I assess the impact of the omissions?
- [ ] Does the overall judgment match the evidence?
- [ ] Is the rationale specific and reproducible?

---

## 20. Evaluation Record Structure

A structured completeness evaluation can use the following fields:

| Field | Description |
|---|---|
| Task | User's original request |
| User Objective | Main intended outcome |
| Requirements | Major requested components |
| Requirement Importance | Critical / Important / Minor |
| Requirement Status | Fully Addressed / Partially Addressed / Not Addressed / N/A |
| Covered Components | Requirements addressed by the response |
| Missing Components | Important requirements not addressed |
| Quantity Check | Whether requested quantities were satisfied |
| Overall Judgment | Complete / Mostly Complete / Partially Complete / Incomplete |
| Evidence | Specific response evidence |
| Rationale | Explanation of the completeness judgment |
| Notes | Additional evaluator observations |

---

## 21. Key Principles

1. Evaluate completeness against the user's actual requirements.
2. Break complex tasks into discrete components.
3. Track each important requirement separately.
4. Distinguish complete coverage from partial coverage.
5. Missing information should be assessed according to its importance.
6. Do not equate response length with completeness.
7. Do not require information that the user did not request unless it is necessary to fulfill the task.
8. Check quantitative requirements explicitly.
9. Evaluate every component of multi-part requests.
10. Support judgments with concrete evidence.
11. Keep completeness distinct from relevance, factuality, and instruction following.
12. The final judgment should follow from the requirement coverage and evidence.

---

## Related Portfolio Sections

- [Instruction Following Framework](../../evaluation-frameworks/instruction-following/README.md)
- [Factuality Framework](../../evaluation-frameworks/factuality/README.md)
- [Relevance Framework](../../evaluation-frameworks/relevance/README.md)

---

## Documentation Scope

This framework is a public portfolio artifact demonstrating a structured approach to AI response evaluation.

Examples and evaluation materials in this repository should use public, synthetic, or anonymized content.

No private evaluation tasks, proprietary datasets, credentials, personally identifiable information, or confidential benchmark materials should be included.
