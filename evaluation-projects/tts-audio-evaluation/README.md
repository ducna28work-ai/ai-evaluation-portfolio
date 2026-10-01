# TTS Audio Evaluation — Fixed-Voice ELO

## Overview

This project demonstrates a structured approach to evaluating two anonymous text-to-speech audio outputs generated from the same transcript.

The evaluation focuses only on audible qualities that can be directly assessed from the audio.

The project does not evaluate:

- Speaker identity
- Target-speaker similarity
- Voice clone realism
- Persona likeness
- Regional voice matching

The evaluation is based on the provided transcript and the audible characteristics of Response A and Response B.

---

## Evaluation Objective

The evaluator compares two anonymous audio clips generated from the same transcript.

The evaluation focuses on four dimensions:

1. Audio and Recording Quality
2. Pronunciation Faithfulness
3. Naturalness
4. Overall Preference

The evaluator must also identify the **Dominant Factor** that explains the overall preference.

The Dominant Factor must correspond to one of the first three evaluation dimensions.

---

## Evaluation Environment

Before evaluation:

- Use headphones when possible.
- Work in a quiet environment.
- Read the provided transcript first.
- Listen to the complete audio for both A and B.
- Replay sections when necessary.
- Judge only what is audibly observable.

Avoid making judgments based on assumptions about the hidden voice prompt or target speaker.

---

# Evaluation Dimensions

## 1. Audio and Recording Quality

Evaluate technical audio quality.

Look for:

- Audible artifacts
- Clipping
- Noise
- Crackling
- Distortion
- Recording problems

Do not use this dimension to evaluate:

- Delivery style
- Pronunciation
- Persona
- Speaker identity

The focus is the technical quality of the recording.

---

## 2. Pronunciation Faithfulness

Evaluate how faithfully the spoken audio represents the provided transcript.

Look for:

- Dropped words
- Added words
- Missing syllables
- Mispronunciations
- Unclear pronunciation
- Incorrect spoken content

The evaluator should compare the audio directly with the transcript.

---

## 3. Naturalness

Evaluate how natural the speech sounds.

Consider:

- Rhythm
- Pacing
- Pauses
- Emphasis
- Intonation
- Overall flow

Naturalness should be judged from the audible speech itself.

---

# 4. Overall Preference

The evaluator must select exactly one preferred response:

```text
Response A
or
Response B
