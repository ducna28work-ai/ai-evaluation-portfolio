# TTS Audio Evaluation

A practical project demonstrating pairwise evaluation of text-to-speech outputs using structured quality dimensions, evidence-based judgments, edge-case handling, and annotation QA.

## Purpose

The project demonstrates how two TTS responses generated from the same transcript can be evaluated consistently using predefined quality dimensions.

The evaluation focuses on observable audio characteristics rather than speaker identity, voice similarity, or persona likeness.

## Evaluation Dimensions

### 1. Audio and Recording Quality

Evaluate whether the audio contains fewer audible technical problems.

Relevant signals include:

- Background noise
- Audible artifacts
- Clipping
- Crackling
- Distortion
- Recording problems

Delivery style and expressiveness should not influence this dimension.

### 2. Pronunciation Faithfulness

Evaluate whether the spoken output accurately follows the transcript.

Relevant signals include:

- Dropped words
- Dropped syllables
- Added words
- Added syllables
- Mispronunciation
- Unclear pronunciation

### 3. Naturalness

Evaluate whether the speech sounds naturally spoken.

Relevant signals include:

- Rhythm
- Pacing
- Pauses
- Emphasis
- Intonation

### 4. Overall Preference

Evaluate which response is better when the relevant dimensions are considered together.

The overall decision should also identify one dominant factor that had the greatest influence on the final preference.

## Evaluation Workflow

**Read Transcript → Listen to A → Listen to B → Evaluate Each Dimension → Compare Evidence → Select Preference → Identify Dominant Factor → QA**

## Pairwise Evaluation

Each evaluation compares two anonymized responses:

```text
Transcript
    │
    ├── Response A
    │
    └── Response B
          ↓
    Dimension-by-Dimension Evaluation
          ↓
    Overall Preference
          ↓
    Dominant Factor
