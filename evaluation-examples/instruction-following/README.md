# Instruction Following — Evaluation Example 📋

A synthetic evaluation example demonstrating how an AI response can be assessed against explicit user requirements.

> **Note:** This is a synthetic example created for portfolio demonstration. It does not contain private evaluation tasks or proprietary platform data.

---

## 🎯 Evaluation Objective

Evaluate whether the AI response follows the user's explicit instructions regarding:

- Number of items
- Language
- Response length
- Content scope

The evaluation focuses specifically on **instruction following**, not factuality.

---

## 🧑 User Task

> Give me **three short reasons** why exercise is beneficial. Answer in **Vietnamese**.

---

## 🤖 AI Response

> Tập thể dục giúp cải thiện sức khỏe tim mạch và tăng sức bền. Nó cũng có thể giúp giảm căng thẳng.

---

## 📋 Requirement Analysis

| Requirement | Type | Assessment |
|---|---|---|
| Provide three reasons | Quantity | ❌ Not satisfied |
| Explain benefits of exercise | Core task | ✅ Satisfied |
| Answer in Vietnamese | Language | ✅ Satisfied |
| Keep the reasons short | Style | ✅ Satisfied |

---

## 🔎 Evidence

### Requirement: Three Reasons

The user explicitly requested **three reasons**.

The response provides two distinct reasons:

1. Improving cardiovascular health and endurance
2. Reducing stress

No third reason is provided.

**Assessment:** Not satisfied.

---

### Requirement: Explain Exercise Benefits

The response explains benefits associated with exercise.

**Assessment:** Satisfied.

---

### Requirement: Vietnamese

The complete response is written in Vietnamese.

**Assessment:** Satisfied.

---

### Requirement: Short Response

The response contains two concise statements and does not introduce unnecessary detail.

**Assessment:** Satisfied.

---

## ⚖️ Overall Judgment

**Partially Compliant**

---

## 🧠 Rationale

The response follows most of the user's requirements, including the requested language, topic, and concise format.

However, the user explicitly requested three reasons and the response provides only two.

Because the missing third reason is a clear requirement of the task, the response does not fully satisfy the instruction.

Therefore, the overall judgment is:

**Partially Compliant**

---

## 🚫 What This Evaluation Does Not Assess

This evaluation focuses on instruction following only.

It does not independently assess:

- Factual accuracy
- Writing quality beyond the requested format
- Safety
- Completeness of the underlying topic
- Usefulness beyond instruction compliance

Those dimensions should be evaluated separately when required by the task.

---

## 📊 Structured Evaluation Record

| Field | Result |
|---|---|
| Task Type | Instruction Following |
| Evaluation Type | Single Response |
| Core Requirement | Provide three short reasons |
| Language Requirement | Vietnamese |
| Quantity Provided | 2 |
| Quantity Required | 3 |
| Overall Judgment | Partially Compliant |
| Primary Error | Missing required item |
| Evidence Available | Yes |

---

## 🧪 Error Category

**Primary Error:** Quantity Error

**Description:** The response does not provide the number of items explicitly requested by the user.

---

## 📌 Key Evaluation Lesson

A response can be relevant, concise, and well-written while still failing to fully follow the user's instructions.

Instruction-following evaluation should therefore verify **explicit requirements individually** before determining the overall judgment.

---

## 🔗 Related Framework

- [Instruction Following Evaluation Framework](../../evaluation-frameworks/instruction-following/)
- [AI Evaluation & Data Quality Portfolio](../../README.md)
