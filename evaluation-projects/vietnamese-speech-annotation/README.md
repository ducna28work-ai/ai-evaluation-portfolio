# Vietnamese Speech Annotation & Quality Assurance

A practical portfolio project demonstrating structured annotation and quality assurance for spontaneous Vietnamese speech.

The project focuses on faithful transcription of spoken audio, including disfluencies, filler words, non-verbal events, pauses, false starts, uncertainty, multiple speakers, dialectal speech, punctuation, written normalization, and audio rejection decisions.

## Purpose

Spontaneous speech is different from polished written language.

Natural speech may contain:

- Filler words
- Hesitations
- False starts
- Repeated words
- Pauses
- Laughter
- Coughing
- Gasping
- Throat clearing
- Background noise
- Unclear speech
- Multiple speakers
- Dialectal expressions
- Informal or colloquial grammar
- Incomplete sentences

The purpose of annotation is not to rewrite this speech into polished Vietnamese.

The objective is to represent what can be heard while applying a consistent annotation convention.

## Golden Rule

> Every audio event should have a corresponding textual event.

If an event can be clearly heard and belongs to the annotation scope, it should be represented in the transcript.

The transcript should therefore preserve:

1. Complete spoken words
2. Supported filler words
3. Word fragments and false starts
4. Supported non-verbal events
5. Meaningful pauses
6. Punctuation reflecting spoken intonation

## Annotation Workflow

```text
Listen to Audio
      ↓
Review Existing Transcript
      ↓
Identify Spoken Words
      ↓
Apply Written Normalization
      ↓
Identify Fillers
      ↓
Identify Non-Verbal Events
      ↓
Handle Unclear / Inaudible Speech
      ↓
Check Foreign-Language Content
      ↓
Identify Speakers
      ↓
Handle Overlap
      ↓
Apply Punctuation
      ↓
Review False Starts
      ↓
Check Dialect and Informal Speech
      ↓
Apply Rejection Rules
      ↓
Final QA
