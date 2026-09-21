# Completeness Evaluation Rubric

## Overview

This rubric provides structured criteria for evaluating whether an AI response adequately covers the important requirements of a user's request.

The rubric focuses on:

- Requirement identification
- Requirement coverage
- Missing components
- Partial coverage
- Quantitative requirements
- Multi-part requests
- Appropriate level of detail
- Importance of omissions
- Evidence-based judgment

Completeness should be evaluated against the user's actual requirements rather than against an expectation that every possible detail must be included.

---

## Overall Judgment

### Complete

The response adequately addresses all important requirements of the task.

Characteristics:

- All major requested components are covered.
- Required quantities are satisfied.
- Requested examples, steps, comparisons, or fields are included.
- No critical omission remains.
- The response provides enough information to fulfill the user's intended outcome.

### Mostly Complete

The response addresses nearly all important requirements but contains a minor omission or limited gap.

Characteristics:

- The main task is fulfilled.
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

## Requirement Status

Evaluate each requirement individually.

| Status | Definition |
|---|---|
| Fully Addressed | The requirement is adequately fulfilled |
| Partially Addressed | The requirement is addressed but important information is missing |
| Not Addressed | The requirement is missing from the response |
| N/A | The requirement does not apply |

The evaluator should identify evidence for partially addressed and missing requirements.

---

## Requirement Importance

Not every requirement has the same impact.

### Critical

Missing the requirement prevents the response from fulfilling the main purpose of the task.

### Important

Missing the requirement creates a meaningful gap but does not completely prevent the user from obtaining value.

### Minor

Missing the requirement has limited impact on the usefulness of the response.

| Importance | Evaluation Question |
|---|---|
| Critical | Does the omission prevent the main task from being fulfilled? |
| Important | Does the omission leave a meaningful gap? |
| Minor | Does the omission have limited practical impact? |

---

## Requirement Coverage

A structured coverage assessment should include:

| Field | Assessment |
|---|---|
| Requirement | Specific requested component |
| Importance | Critical / Important / Minor |
| Status | Fully Addressed / Partially Addressed / Not Addressed / N/A |
| Evidence | Where the response addresses or misses it |
| Notes | Additional observation |

---

## Quantitative Requirements

When the user specifies a quantity, evaluate it explicitly.

Examples:

- "Give me five examples."
- "List three benefits."
- "Provide ten keywords."
- "Give me two alternatives."

### Example

Requested:

> Five examples.

Provided:

> Three examples.

Assessment:

- Quantity requirement: Partially Addressed
- Missing components: Two examples
- Completeness issue: Missing Requested Items

The evaluator should not consider the requirement complete simply because the provided items are relevant.

---

## Multi-Part Requests

For multi-part requests, evaluate each major component independently.

Example:

> "Explain GA4, compare it with Universal Analytics, and give three practical use cases."

| Component | Status |
|---|---|
| Explain GA4 | Fully Addressed / Partially Addressed / Not Addressed |
| Compare with Universal Analytics | Fully Addressed / Partially Addressed / Not Addressed |
| Provide three use cases | Fully Addressed / Partially Addressed / Not Addressed |

The final judgment should consider the importance and number of missing components.

---

## Procedural Tasks

For "how to" requests, evaluate whether the response contains the important steps required to accomplish the requested task.

Consider:

- Required setup
- Main actions
- Important configuration
- Necessary verification
- Relevant final step

Do not require every possible optional detail.

The evaluator should assess whether the user could reasonably accomplish the requested outcome using the information provided.

---

## Comparison Tasks

For comparison requests, completeness depends on the requested comparison dimensions.

Example:

> "Compare Tool A and Tool B based on price, features, and ease of use."

Required dimensions:

- Price
- Features
- Ease of use

A response covering only features is incomplete because two requested comparison dimensions are missing.

---

## Examples and Supporting Information

If the user explicitly requests examples, examples are part of the completeness requirement.

If examples are not requested, they are generally optional.

Additional information should only be treated as necessary when it is required to fulfill the user's intended outcome.

---

## Completeness vs. Relevance

These dimensions should remain separate.

### Complete but Irrelevant

A response could contain many details and fully cover a different task.

It may be comprehensive but still irrelevant to the user's request.

### Relevant but Incomplete

A response may stay completely focused on the correct topic but omit important requested components.

Example:

> User asks for five SEO benefits.

Response provides two accurate SEO benefits.

The response is relevant, but incomplete.

---

## Completeness vs. Length

Do not use word count as the primary completeness criterion.

### Long Response

A long response may still be incomplete if it omits important requested components.

### Short Response

A short response may be complete if it adequately fulfills a simple request.

The evaluator should assess whether the necessary information is present.

---

## Severity of Completeness Issues

### Minor

A small requested detail is missing, but the main task is fulfilled.

### Major

One or more important components are missing and the omission meaningfully reduces task fulfillment.

### Critical

A critical requirement is missing and the response cannot reasonably fulfill the user's primary objective.

| Severity | Typical Impact |
|---|---|
| Minor | Limited impact |
| Major | Meaningful reduction in task fulfillment |
| Critical | Main objective cannot reasonably be fulfilled |

Severity should be based on the importance and impact of the omission, not simply the number of missing words or sentences.

---

## Evidence Standard

Every completeness judgment should be supported by concrete evidence.

### Strong Evidence

> "The user requested three benefits and one example for each. The response provides all three benefits but gives examples for only two, leaving one requested component missing."

### Weak Evidence

> "The answer needs more information."

A strong rationale identifies:

1. What the user requested.
2. What the response provided.
3. What is missing.
4. Why the omission matters.

---

## Recommended Evaluation Record

```text
Task:
User Objective:

Requirements:
1.
2.
3.

Requirement Importance:
1.
2.
3.

Requirement Status:
1.
2.
3.

Covered Components:
Missing Components:

Quantity Check:

Overall Judgment:
Issue Type:
Severity:

Evidence:
Rationale:
Notes:
