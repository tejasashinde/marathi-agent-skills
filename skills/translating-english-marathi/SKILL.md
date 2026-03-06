---
name: translating-english-marathi
description: >
  Translates text between English and Marathi and vice-versa. Use when the user asks to translate text between English and Marathi, convert English into Marathi, convert Marathi into English, or requests Marathi translation, English translation or bilingual conversion.
---

# Translating English Marathi

Precise bidirectional translation between English and Marathi while preserving meaning, grammar, and tone. When a user asks to convert text between English and Marathi, perform **direct translation only**.

DO NOT:
- Explain the translation or Add commentary
- Paraphrase the content
- Change the meaning

Return ONLY the translated text or translated file content.

## Quick start

**OPERATING MODES** See operating modes section below
**WORKFLOW** See workflow section below
**OUTPUT RULES** See output rules section below
**EXAMPLES** See [EXAMPLES.md](EXAMPLES.md) for common patterns
**TRANSLATION STANDARD** See translation standard section below

---

# OPERATING MODES

Operates in **two modes depending on user input**.

## Mode 1 — Inline Text Translation

Use when the user provides text directly in the message. Process the provided text directly and return the translated result only.

---

## Mode 2 — File Translation

Use when the user provides or references a file containing text to translate.

Supported file formats:
- `.txt`
- `.docx`
- `.csv`
- `.pdf`

Process the file contents and return the translated version while preserving structure where possible.

File handling rules:
- `.txt` -> translate entire text sequentially
- `.docx` -> translate paragraph by paragraph
- `.csv` -> translate cell values containing language text
- `.pdf` -> extract readable text then translate sequentially

Preserve:
- sentence order
- document structure
- table structure (for CSV)

Do NOT translate:
- URLs
- file paths
- code snippets

---

## File With Mixed Content

If a file contains:
- numbers
- URLs
- technical identifiers

Translate only natural language text and leave other data unchanged.

---

# WORKFLOW

## 1. Detect Source Language

Determine the language of the provided text.

Indicators:

**English**
- Latin alphabet
- English vocabulary and grammar

**Marathi**
- Devanagari script
- Marathi vocabulary and sentence structure

Translation direction:

- English -> Marathi  
- Marathi -> English

---

## 2. Translate Meaning, Not Words

Perform **meaning-preserving translation**.

Ensure:
- Sentence meaning is preserved
- Tone remains consistent
- Grammar is correct
- Output sounds natural to native speakers

Avoid:
- Literal word-by-word translation
- Grammar distortion
- Meaning alteration

---

## 3. Marathi Generation Rules

When producing Marathi text:
Use:
- Proper **Devanagari script**
- Natural Marathi sentence structure
- Native vocabulary

Avoid:
- Hindi substitutions
- Mixed-language output
- Phonetic transliteration

---

## 4. English Generation Rules

When translating Marathi -> English:

Ensure:
- Natural English grammar
- Correct tense usage
- Clear sentence structure

Avoid:
- Literal structure transfer
- Broken English

---

# OUTPUT RULES

Inline Mode:
Return only the translated text.

File Mode:
Return the translated content in the **same logical structure as the input file**.

Do not include:
- explanations
- commentary
- metadata
- additional formatting

Multiple sentences must be translated completely while preserving their sequence.

---

# EXAMPLES

See [EXAMPLES.md](EXAMPLES.md) for common patterns.

---

# TRANSLATION STANDARD

Every translation must be:
- grammatically correct
- contextually accurate
- natural sounding
- faithful to the original meaning

Never invent information that does not exist in the source text.

---