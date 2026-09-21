# Relevance Evaluation Rubric

## Overview

This rubric provides structured criteria for evaluating whether an AI response is relevant to the user's request.

The rubric focuses on:

- User intent
- Topic alignment
- Scope control
- Directness
- Coverage of requested components
- Tangential content
- Unnecessary expansion
- Evidence-based judgment

Relevance should be evaluated against the user's actual goal rather than individual keywords.

---

## Overall Judgment

### Highly Relevant

The response directly addresses the user's intent and stays within the appropriate scope.

Characteristics:

- Clearly addresses the main request.
- Covers the important requested components.
- Maintains strong topical alignment.
- Contains little or no tangential content.
- Uses additional context only when it supports the user's goal.
- Maintains appropriate scope and focus.

### Mostly Relevant

The response addresses the main intent and is generally focused, but contains minor tangential or unnecessary content.

Characteristics:

- Main request is addressed.
- Most content contributes to the requested outcome.
- Some secondary information is unnecessary.
- Minor scope or focus issues may exist.
- The additional content does not substantially prevent the user from obtaining the requested information.

### Partially Relevant

The response addresses part of the user's intent but has meaningful relevance problems.

Characteristics:

- Important requested components may be missing.
- Significant tangential content may be present.
- The response may shift toward related but unrequested topics.
- Scope control is weak.
- The response provides some useful information but does not adequately address the overall request.

### Not Relevant

The response does not meaningfully address the user's primary intent.

Characteristics:

- Focuses on a substantially different topic.
- Does not provide the requested information.
- May contain keywords related to the topic without addressing the underlying request.
- Most of the response is outside the appropriate scope.

---

## Relevance Dimensions

### 1. User Intent

| Status | Description |
|---|---|
| Strongly Aligned | Response clearly addresses the user's primary goal |
| Partially Aligned | Response addresses part of the user's goal |
| Weakly Aligned | Response has limited connection to the user's goal |
| Not Aligned | Response does not address the user's goal |

---

### 2. Topic Alignment

| Status | Description |
|---|---|
| Strong | Response consistently stays on the requested topic |
| Moderate | Response is mostly on topic with some related tangents |
| Weak | Response frequently shifts to related but unrequested topics |
| None | Response primarily discusses a different topic |

---

### 3. Scope Control

| Status | Description |
|---|---|
| Appropriate | Content stays within the expected scope |
| Minor Expansion | Some additional content is unnecessary but does not substantially distract |
| Excessive Expansion | Significant space is spent on secondary or unrequested topics |
| Incorrect Scope | Response primarily operates outside the requested scope |

---

### 4. Directness

| Status | Description |
|---|---|
| Direct | Response efficiently addresses the main request |
| Mostly Direct | Main request is addressed with minor unnecessary material |
| Indirect | User's request is addressed only partially or after substantial tangents |
| Not Direct | Response does not meaningfully address the request |

---

### 5. Requested Coverage

For multi-part requests, evaluate whether the major requested components are addressed.

| Status | Description |
|---|---|
| Complete | All major requested components are addressed |
| Mostly Complete | Most major components are addressed |
| Partial | Some important components are missing |
| Minimal/None | Most or all requested components are missing |

---

## Relevance Issue Types

### Off-Topic Response

The response addresses a substantially different subject.

**Example:**

User asks for SEO benefits of internal linking, but the response primarily explains social media marketing.

---

### Tangential Content

The content is related to the general topic but does not materially contribute to answering the request.

**Example:**

User asks for three internal linking benefits, but the response spends a long section discussing backlink acquisition.

---

### Partial Topic Coverage

The response addresses only part of the requested topic.

**Example:**

User asks for three benefits but the response explains only one.

---

### Over-Expansion

The response contains excessive secondary information that reduces focus.

**Example:**

A simple definition is followed by several paragraphs of unrelated history.

---

### Keyword Matching Without Intent

The response contains relevant keywords but does not address the actual question.

**Example:**

User asks how internal links improve SEO, while the response defines "SEO" and "internal links" without explaining their relationship.

---

### Under-Focused Response

The response contains useful information but fails to prioritize the user's main need.

---

## Context Relevance

Additional context should not automatically be classified as irrelevant.

Evaluate whether the information:

- Clarifies the answer.
- Prevents misunderstanding.
- Supports the requested task.
- Provides a useful example.
- Explains an important limitation.
- Helps the user apply the answer.

If the context performs one of these functions, it may remain relevant even if it is not the direct answer.

---

## Relevance vs. Length

Length should not be used as a direct proxy for relevance.

### Long and Relevant

A detailed response can be highly relevant when each section contributes to the user's goal.

### Short and Irrelevant

A short response can still be irrelevant if it does not address the actual request.

The evaluator should judge **content contribution**, not word count.

---

## Multi-Part Request Evaluation

When a request contains multiple components, evaluate each major component separately.

Example:

> "Explain GA4, compare it with Universal Analytics, and give three use cases."

| Component | Evaluation |
|---|---|
| Explain GA4 | Addressed / Missing |
| Compare with Universal Analytics | Addressed / Missing |
| Provide three use cases | Addressed / Missing |

The overall relevance judgment should consider the combined coverage and importance of the missing components.

---

## Evidence Standard

A relevance judgment should be supported by specific evidence.

### Strong Evidence

> "The response provides the three requested benefits but adds an unrelated discussion of backlink building."

### Weak Evidence

> "The response is a little off-topic."

The rationale should explain **what was relevant, what was not, and why**.

---

## Evaluation Severity

Relevance issues can be categorized by impact.

### Minor

The response is still useful and focused, but contains small amounts of unnecessary content.

### Major

The response contains substantial tangents, misses important parts of the request, or significantly reduces focus.

### Critical

The response fails to meaningfully address the user's primary request.

Severity should describe the impact of the relevance issue, not simply the amount of text involved.

---

## Recommended Evaluation Record

```text
Task:
User Intent:
Scope:
Core Requirements:

User Intent Alignment:
Topic Alignment:
Scope Control:
Directness:
Requested Coverage:

Relevant Content:
Tangential Content:
Irrelevant Content:
Missing Content:

Issue Type:
Severity:
Overall Judgment:

Evidence:
Rationale:
