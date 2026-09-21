# Relevance Evaluation Framework

## Overview

Relevance evaluation assesses whether an AI response directly addresses the user's request and stays within the appropriate scope.

A relevant response focuses on the user's actual intent, provides information that contributes to the requested outcome, and avoids unnecessary tangents.

Relevance is different from factuality or instruction following:

- **Relevance:** Does the response address the right topic and user need?
- **Instruction Following:** Does the response follow the explicit requirements and constraints?
- **Factuality:** Are the claims accurate and supported?

A response can be factually correct but still be irrelevant if it does not address the user's actual request.

---

## Evaluation Objective

The evaluator should determine whether the response:

1. Understands the user's primary intent.
2. Addresses the requested topic or problem.
3. Covers the appropriate scope.
4. Prioritizes information that is useful for the task.
5. Avoids unrelated or unnecessary content.
6. Maintains focus throughout the response.
7. Provides context only when it contributes to the user's goal.

The evaluation should focus on the relationship between the **user's request** and the **content of the response**.

---

## Evaluation Workflow

**Understand User Intent → Identify Scope → Identify Core Requirements → Review Response → Assess Relevance → Identify Evidence → Make Judgment → Record Rationale → Quality Check**

---

## 1. Understand User Intent

Before evaluating relevance, identify what the user is actually trying to accomplish.

Consider:

- What question is the user asking?
- What information are they requesting?
- What outcome do they expect?
- Is the request informational, procedural, analytical, creative, or transactional?
- Are there multiple explicit questions?

Do not evaluate relevance based only on individual keywords.

The evaluator should consider the overall meaning and purpose of the request.

### Example

User request:

> "What are the main benefits of using internal links in SEO?"

The primary intent is to understand the SEO benefits of internal linking.

A response discussing the history of search engines without connecting it to internal linking would have limited relevance even if the information is accurate.

---

## 2. Identify Scope

Determine the appropriate scope of the response before reviewing its content.

Scope may include:

- Topic
- Subtopics
- Requested depth
- Requested format
- Number of items
- Time period
- Geographic scope
- Target audience
- Specific entities or examples

The evaluator should distinguish between information that is outside the requested scope and information that provides necessary context.

---

## 3. Identify Core Requirements

Break the request into its main information needs.

For example:

> "Give me three reasons why internal linking is useful for SEO."

Core requirements:

- Explain benefits of internal linking.
- Focus on SEO.
- Provide three reasons.

The relevance assessment should primarily consider whether the response addresses these core information needs.

---

## 4. Review the Response

Read the complete response and identify the relationship between each major section and the user's request.

Ask:

- Does the response answer the question?
- Does each major point contribute to the requested outcome?
- Does the response remain focused?
- Are there unnecessary tangents?
- Does the response spend too much space on secondary information?
- Does the response introduce topics that the user did not ask about?

Evaluate the response as a whole rather than judging relevance from a single sentence.

---

## 5. Assess Directness

Directness measures how efficiently the response addresses the user's actual need.

A direct response:

- Answers the main question early.
- Prioritizes relevant information.
- Avoids unnecessary detours.
- Uses supporting details when they help answer the question.

A response does not need to be extremely short to be relevant.

Additional explanation can still be relevant when it improves understanding or supports the requested task.

---

## 6. Assess Topical Alignment

Check whether the response stays aligned with the topic identified from the user's request.

### Strong topical alignment

The response consistently discusses the subject requested by the user.

### Weak topical alignment

The response begins with the requested topic but gradually shifts toward related subjects that do not materially help answer the request.

### No topical alignment

The response primarily discusses a different subject from the user's request.

---

## 7. Detect Irrelevant or Tangential Content

Identify content that does not materially contribute to the user's requested outcome.

Common examples include:

- Unrelated background information.
- Unrequested recommendations.
- Long historical explanations when not needed.
- Personal opinions unrelated to the task.
- Repetition that adds no useful information.
- Discussion of a different topic.
- Excessive disclaimers that do not address a meaningful risk.
- Unnecessary examples that distract from the main answer.

Not every additional detail is irrelevant.

The evaluator should ask:

> "Does this information help answer the user's request?"

If the answer is no, the content may be considered irrelevant or tangential.

---

## 8. Distinguish Useful Context from Irrelevant Content

Some information may not directly answer the question but is still relevant because it helps the user understand or apply the answer.

### Useful context

Context can be relevant when it:

- Clarifies an important concept.
- Explains a necessary limitation.
- Helps interpret the answer.
- Prevents a likely misunderstanding.
- Supports the requested decision or task.
- Provides a directly relevant example.

### Irrelevant context

Context becomes problematic when it:

- Does not affect the answer.
- Introduces unrelated subjects.
- Takes substantial space without improving understanding.
- Distracts from the user's main objective.

The evaluator should consider the function of the information, not simply whether it is additional.

---

## 9. Assess Scope Control

A strong response maintains an appropriate balance between completeness and focus.

Evaluate whether the response:

- Covers the important aspects of the request.
- Avoids unnecessary expansion.
- Gives appropriate attention to the main question.
- Does not allow secondary topics to dominate the response.

A response can be detailed and still be highly relevant.

The issue is not length itself, but whether the content contributes to the user's goal.

---

## 10. Multi-Part Requests

For requests containing multiple questions or tasks, evaluate relevance for each major component.

For example:

> "Explain what GA4 is, how it differs from Universal Analytics, and give three practical use cases."

The response should address:

1. What GA4 is.
2. How it differs from Universal Analytics.
3. Three practical use cases.

A response that thoroughly explains GA4 but ignores the comparison and use cases is not fully relevant to the overall request.

---

## 11. Handling Ambiguous Requests

When a request is ambiguous, evaluate the response against the most reasonable interpretation supported by the user's wording.

A relevant response may:

- State the interpretation being used.
- Ask a clarifying question when necessary.
- Provide a reasonable answer while identifying the ambiguity.
- Address the most likely intent without introducing unrelated topics.

Do not penalize a response simply because the request allows multiple reasonable interpretations.

---

## 12. Relevance Errors

Common relevance problems include:

### Off-Topic Response

The response addresses a substantially different topic.

### Tangential Response

The response discusses the requested topic but spends significant attention on related subjects that do not help answer the question.

### Under-Focused Response

The response contains relevant information but does not prioritize the user's primary need.

### Over-Expansion

The response adds excessive secondary information that reduces focus.

### Partial Topic Coverage

The response addresses one part of a multi-part request while ignoring other relevant parts.

### Keyword Matching Without Intent

The response mentions the user's keywords but does not actually address the underlying question.

---

## 13. Overall Judgment

Use the following relevance scale:

### Highly Relevant

The response directly addresses the user's intent, stays within the appropriate scope, and contains little or no irrelevant content.

### Mostly Relevant

The response addresses the main intent and is generally focused, but contains some minor tangential or unnecessary content.

### Partially Relevant

The response addresses part of the user's intent but has meaningful gaps, unnecessary tangents, or poor scope control.

### Not Relevant

The response does not meaningfully address the user's primary intent or focuses on a substantially different topic.

The overall judgment should reflect the response as a whole.

---

## 14. Evidence-Based Evaluation

Relevance judgments should be supported by observable evidence from the response.

Useful evidence includes:

- Specific sections that answer the user's question.
- Specific requested components that were addressed.
- Specific tangential sections.
- Missing parts of a multi-part request.
- Examples showing whether the response stayed within scope.

Avoid vague rationales such as:

> "The answer feels irrelevant."

Prefer:

> "The response explains the requested SEO concept but spends most of its length discussing website design, which was not part of the user's request."

---

## 15. Edge Cases

### Necessary Caveats

A short caveat may remain relevant when it materially affects the answer.

Do not classify every disclaimer as irrelevant.

### Relevant Examples

Examples should generally be considered relevant when they clarify the requested concept or help the user apply the answer.

### Related Information

Related information is not automatically relevant.

The evaluator should determine whether it contributes to the user's stated goal.

### Long but Relevant Responses

A long response can still be highly relevant if the additional information consistently supports the user's request.

### Short but Irrelevant Responses

A short response can still be irrelevant if it does not address the user's actual intent.

### Follow-Up Context

Information from earlier parts of a conversation may be relevant even when it is not repeated in the latest user message.

The evaluator should consider the available conversation context when the evaluation task provides it.

---

## 16. Quality Assurance Checklist

Before finalizing a relevance evaluation, check:

- [ ] Did I identify the user's primary intent?
- [ ] Did I identify the appropriate scope?
- [ ] Did I identify the main information requirements?
- [ ] Did I review the response as a whole?
- [ ] Did I distinguish useful context from irrelevant content?
- [ ] Did I check for tangents?
- [ ] Did I check all parts of a multi-part request?
- [ ] Did I avoid treating response length as relevance by itself?
- [ ] Did I identify concrete evidence?
- [ ] Does the final judgment match the evidence?
- [ ] Is the rationale specific and reproducible?

---

## 17. Evaluation Record Structure

A structured relevance evaluation can use the following fields:

| Field | Description |
|---|---|
| Task | User's original request |
| User Intent | Primary goal of the request |
| Scope | Appropriate boundaries for the response |
| Core Requirements | Main information needs |
| Response Summary | Brief description of what the response provides |
| Relevant Content | Evidence that directly addresses the task |
| Tangential Content | Content that is related but not necessary |
| Irrelevant Content | Content unrelated to the task |
| Missing Content | Important requested elements that were not addressed |
| Overall Judgment | Highly Relevant / Mostly Relevant / Partially Relevant / Not Relevant |
| Rationale | Evidence-based explanation |
| Notes | Additional evaluator observations |

---

## 18. Key Principles

1. Evaluate relevance against the user's intent, not isolated keywords.
2. Relevant information should contribute to the requested outcome.
3. Additional context is acceptable when it serves a clear purpose.
4. Related information is not automatically relevant.
5. Response length alone does not determine relevance.
6. Multi-part requests should be evaluated across all major components.
7. Relevance judgments should be supported by observable evidence.
8. Keep relevance distinct from factuality and instruction following.
9. Use consistent criteria across evaluations.
10. The final judgment should follow the evidence and rationale.

---

## Related Portfolio Sections

- [Instruction Following Framework](../../evaluation-frameworks/instruction-following/README.md)
- [Factuality Framework](../../evaluation-frameworks/factuality/README.md)

---

## Documentation Scope

This framework is a public portfolio artifact demonstrating a structured approach to AI response evaluation.

Examples and evaluation materials in this repository should use public, synthetic, or anonymized content.

No private evaluation tasks, proprietary datasets, credentials, personally identifiable information, or confidential benchmark materials should be included.
