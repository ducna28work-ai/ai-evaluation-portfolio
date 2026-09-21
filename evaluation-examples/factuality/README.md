# Factuality & Accuracy — Evaluation Example 🔎

A synthetic evaluation example demonstrating how factual claims in an AI-generated response can be assessed against provided reference information.

> **Note:** This is a synthetic example created for portfolio demonstration. It does not contain private evaluation tasks or proprietary platform data.

---

## 🎯 Evaluation Objective

Evaluate whether the AI response accurately represents the information provided in the reference material.

The evaluation focuses specifically on:

- Factual claims
- Evidence alignment
- Contradictions
- Error severity
- Evidence-based rationale

---

## 🧑 User Task

> According to the information provided below, which city is the capital of Country A?

---

## 📚 Reference Information

> The capital of Country A is **City X**.

---

## 🤖 AI Response

> The capital of Country A is **City Y**.

---

## 🔎 Claim Analysis

The response contains one primary factual claim:

> The capital of Country A is City Y.

This claim can be directly compared against the provided reference information.

---

## 📋 Evidence Assessment

| Claim | Reference Evidence | Assessment |
|---|---|---|
| Country A's capital is City Y | The reference states that the capital is City X | ❌ Incorrect |

---

## ⚠️ Error Classification

**Error Type:** Incorrect Fact

**Severity:** Major

### Reason

The response directly contradicts the provided reference information.

The reference identifies **City X** as the capital, while the response identifies **City Y**.

---

## ⚖️ Overall Judgment

**Inaccurate**

---

## 🧠 Rationale

The response makes a factual claim that directly contradicts the available reference information.

Because the incorrect capital is the central answer to the user's question, the error materially affects the correctness of the response.

Therefore, the response is classified as **Inaccurate**.

---

## 🚫 What This Evaluation Does Not Assess

This evaluation focuses on factual accuracy.

It does not independently assess:

- Instruction following
- Writing style
- Helpfulness
- Completeness beyond the factual claim
- Safety
- Tone

These dimensions may require separate evaluation criteria.

---

## 📊 Structured Evaluation Record

| Field | Result |
|---|---|
| Task Type | Factuality & Accuracy |
| Evaluation Type | Single Response |
| Reference Available | Yes |
| Factual Claims | 1 |
| Supported Claims | 0 |
| Incorrect Claims | 1 |
| Primary Error | Incorrect Fact |
| Error Severity | Major |
| Overall Judgment | Inaccurate |

---

## 🔬 Evidence-Based Reasoning

The evaluation follows a direct evidence chain:

**Reference Information → Response Claim → Comparison → Contradiction → Error Classification → Severity → Judgment**

This makes the evaluation reproducible because another evaluator can review the same evidence and understand how the judgment was reached.

---

## 📌 Key Evaluation Lesson

A factuality evaluation should not rely on whether an answer sounds plausible.

The evaluator should identify the factual claim and compare it against the evidence available for the task.

When the claim directly contradicts reliable reference information, the contradiction should be explicitly documented and reflected in the evaluation judgment.

---

## 🔗 Related Portfolio Sections

- [Factuality & Accuracy Framework](../../evaluation-frameworks/factuality/)
- [AI Evaluation & Data Quality Portfolio](../../README.md)
