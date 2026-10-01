# Vietnamese Speech Annotation QA Rubric

## Purpose

This rubric is used to evaluate whether an annotation faithfully represents the audio and consistently applies the project rules.

The rubric separates transcription accuracy from formatting, normalization, event annotation, and rejection decisions.

---

# 1. Speech Fidelity

## Good

- All understandable spoken words are represented.
- No unsupported words are added.
- Informal grammar is preserved.
- Complete repeated words remain.
- Dialectal speech remains recognizable.

## Bad

- Words are omitted.
- Words are invented.
- Speech is rewritten into polished prose.
- Repeated words are removed.
- Dialect is silently standardized.

---

# 2. Written Normalization

Check whether the annotation correctly applies defined normalization rules for:

- Numbers
- Dates
- Times
- Currency
- Percentages
- Fractions
- Addresses
- Measurements
- Names containing special symbols

## Good

```text
bốn mươi hai
→ 42
