# Human vs LLM Judge — Comparison

This comparison uses synthetic human-style and LLM judge evaluations based on the shared AI Evaluation Benchmark.

The examples are designed to demonstrate how agreement, partial agreement, and disagreement can be reviewed using the same evaluation criteria.

## Comparison 1 — Instruction Following

**Task ID:** BENCH-003

**Dimension:** Instruction Following

**Task:** Write a 100-word introduction to technical SEO for beginners.

| Field | Human-Style Evaluation | LLM Judge |
|---|---|---|
| Judgment | Partially Compliant | Fully Compliant |
| Evidence | The response exceeds the explicit 100-word constraint. | The response explains technical SEO clearly for beginners. |
| Rationale | The topic and audience requirements are satisfied, but the quantitative constraint is not. | The core request is addressed and the explanation is suitable for beginners. |

**Agreement:** Disagreement

**Error Type:** Requirement Omission

**Review:** The human-style evaluation identifies the explicit word-count constraint, while the LLM judge focuses on topical and audience alignment.

**Final Assessment:** Partially Compliant

**Reasoning:** The quantitative requirement is explicit and should be evaluated independently from topical correctness.

---

## Comparison 2 — Factuality

**Task ID:** BENCH-010

**Dimension:** Factuality

**Task:** Does a higher keyword density guarantee higher Google rankings?

| Field | Human-Style Evaluation | LLM Judge |
|---|---|---|
| Judgment | Inaccurate | Mostly Accurate |
| Evidence | The response presents keyword density as a ranking guarantee. | The response discusses the relationship between keywords and rankings. |
| Rationale | The deterministic claim is unsupported. | The response appears to describe keyword usage as relevant to SEO. |

**Agreement:** Disagreement

**Error Type:** Evidence Mismatch

**Review:** The human-style evaluation focuses on the absolute claim that higher keyword density guarantees higher rankings. The LLM judge gives greater weight to the general topic of keyword usage.

**Final Assessment:** Inaccurate

**Reasoning:** The specific guarantee is the material factual claim being evaluated.

---

## Comparison 3 — Relevance

**Task ID:** BENCH-016

**Dimension:** Relevance

**Task:** Give three examples of informational keywords.

| Field | Human-Style Evaluation | LLM Judge |
|---|---|---|
| Judgment | Mostly Relevant | Highly Relevant |
| Evidence | The requested examples are provided, but the response includes an unnecessary domain-authority tangent. | The response provides the requested examples and remains broadly related to SEO. |
| Rationale | The additional tangent reduces directness. | The extra information remains within the broader SEO topic. |

**Agreement:** Disagreement

**Error Type:** Scope Interpretation

**Review:** Both evaluations recognize that the requested examples are present. The disagreement concerns whether the additional information materially affects relevance.

**Final Assessment:** Mostly Relevant

**Reasoning:** The task asks for three examples, so unnecessary additional content can reduce directness even when it remains topically related.

---

## Comparison 4 — Completeness

**Task ID:** BENCH-023

**Dimension:** Completeness

**Task:** List five types of search intent.

| Field | Human-Style Evaluation | LLM Judge |
|---|---|---|
| Judgment | Incomplete | Mostly Complete |
| Evidence | Four types are listed instead of the requested five. | Four valid types are provided and the main concept is addressed. |
| Rationale | The explicit quantity requirement is not satisfied. | The response demonstrates understanding despite one missing item. |

**Agreement:** Disagreement

**Error Type:** Requirement Omission

**Review:** The human-style evaluation applies the explicit quantitative requirement. The LLM judge places greater emphasis on conceptual coverage.

**Final Assessment:** Incomplete

**Reasoning:** The task explicitly requests five items, but only four are provided.

---

## Comparison 5 — Response Quality

**Task ID:** BENCH-027

**Dimension:** Response Quality

**Task:** Explain canonical tags.

| Field | Human-Style Evaluation | LLM Judge |
|---|---|---|
| Judgment | Poor Quality | Fair Quality |
| Evidence | The response mentions canonical tags but does not clearly explain the concept. | The response identifies the correct topic and provides some relevant information. |
| Rationale | Topic recognition alone does not make the explanation useful. | The answer contains relevant information but lacks depth. |

**Agreement:** Partial Agreement

**Error Type:** Quality Threshold

**Review:** Both evaluations identify limited explanation quality. The difference is primarily the threshold used to distinguish Poor from Fair quality.

**Final Assessment:** Poor Quality

**Reasoning:** A useful explanation should clearly communicate the requested concept rather than merely mention it.

---

## Comparison 6 — Factuality

**Task ID:** BENCH-036

**Dimension:** Factuality

**Task:** Can an XML sitemap guarantee that every listed URL will be indexed by Google?

| Field | Human-Style Evaluation | LLM Judge |
|---|---|---|
| Judgment | Inaccurate | Inaccurate |
| Evidence | The response makes an absolute indexing guarantee. | The response states that sitemap inclusion leads to indexing. |
| Rationale | A sitemap does not guarantee indexing. | The claim is too absolute. |

**Agreement:** Agreement

**Error Type:** None

**Review:** Both evaluations identify the unsupported absolute claim.

**Final Assessment:** Inaccurate

**Reasoning:** Both judgments are supported by the same factual issue in the response.

---

## Summary

| Task ID | Dimension | Human Judgment | LLM Judgment | Agreement | Error Type |
|---|---|---|---|---|---|
| BENCH-003 | Instruction Following | Partially Compliant | Fully Compliant | Disagreement | Requirement Omission |
| BENCH-010 | Factuality | Inaccurate | Mostly Accurate | Disagreement | Evidence Mismatch |
| BENCH-016 | Relevance | Mostly Relevant | Highly Relevant | Disagreement | Scope Interpretation |
| BENCH-023 | Completeness | Incomplete | Mostly Complete | Disagreement | Requirement Omission |
| BENCH-027 | Response Quality | Poor Quality | Fair Quality | Partial Agreement | Quality Threshold |
| BENCH-036 | Factuality | Inaccurate | Inaccurate | Agreement | None |

## Observed Patterns

The synthetic comparisons demonstrate several potential sources of human-vs-LLM judgment differences:

1. Explicit quantitative requirements may be underweighted.
2. General topical correctness may receive more weight than a specific factual claim.
3. Relevance judgments may differ based on tolerance for tangential information.
4. Completeness judgments may differ when some requested components are missing.
5. Response quality judgments may vary around quality thresholds.
6. Clear factual errors can produce agreement when both evaluators identify the same evidence.

## QA Principle

The comparison should not assume that agreement means correctness or disagreement means that one evaluator is automatically wrong.

Each difference should be reviewed against:

**Task Requirements → Evaluation Criteria → Response Evidence → Judgment → Rationale**

## Limitations

These comparison records are synthetic portfolio examples.

They do not measure the performance of a real LLM judge or represent a production evaluation benchmark.
