---
name: marathi-transliterator
description: >
  Transliterates English into Marathi and vice-versa. Use when the user explicitly asks for transliteration between Marathi and English languages only. DO NOT USE for translation.
---

# Marathi Transliterator

Performs deterministic script conversion between Marathi (Devanagari) and Roman letters.

You are performing **script transliteration only**.
If the user provides Marathi text, convert characters to Roman letters using the defined phonemic mapping.
If the user provides Romanized Marathi, convert it into valid Devanagari script.
If ambiguity exists - ask for clarification. Do not guess.

Do NOT translate meaning between Marathi and English. Words must remain identical phonetically. Only the writing system changes.
Example: राम -> rām
NOT: hello -> नमस्कार

---

## When to Use This Skill

Load this skill when user says:
- “Transliterate Marathi to English letters.”
- “Convert Roman to Marathi script.”
- “Write this Marathi in Latin alphabet.”
- “Give Marathi in Roman letters.”
- “Convert this Roman Marathi into Devanagari.”

Do NOT load this skill for:
- English to Marathi translation
- Marathi to English translation
- Grammar correction or Meaning explanation
- Meaning translation.
- Grammar correction.
- Paraphrasing.
- Language explanation.

---

## WORKFLOW

### 1. Detect Script Direction

- If Input contains Devanagari characters (e.g., म, क, आ, ण) -> Convert to Roman.
- If input contains Latin letters that resemble Romanized Marathi phonetics (e.g., aa, ā, bh, dh, kṣ), convert to Marathi.
- If the text is clearly English language content, do NOT transliterate and ask the user for confirmation.
- If mixed or ambiguous -> Ask user to confirm intended direction if not specified.

No assumptions.

---

### 2. Apply Deterministic Mapping

Use the exact phonemic mapping below.

# Marathi to Roman Transliteration Mapping

## 1. Independent Vowels
अ  -> a
आ  -> ā
इ  -> i
ई  -> ī
उ  -> u
ऊ  -> ū
ए  -> e
ऐ  -> ai
ओ  -> o
औ  -> au
अं -> aṃ
अः -> aḥ

## 2. Consonants
क  -> k
ख  -> kh
ग  -> g
घ  -> gh
ङ  -> ṅ
च  -> c
छ  -> ch
ज  -> j
झ  -> jh
ञ  -> ñ
ट  -> ṭ
ठ  -> ṭh
ड  -> ḍ
ढ  -> ḍh
ण  -> ṇ
त  -> t
थ  -> th
द  -> d
ध  -> dh
न  -> n
प  -> p
फ  -> ph
ब  -> b
भ  -> bh
म  -> m
य  -> y
र  -> r
ल  -> l
व  -> v
श  -> ś
ष  -> ṣ
स  -> s
ह  -> h
झ  -> z

## 3. Dependent Vowel Signs (Matras)
ा  -> ā      (का -> kā)
ि  -> i      (कि -> ki)
ी  -> ī      (की -> kī)
ु  -> u      (कु -> ku)
ू  -> ū      (कू -> kū)
े  -> e      (के -> ke)
ै  -> ai     (कै -> kai)
ो  -> o      (को -> ko)
ौ  -> au     (कौ -> kau)
ं  -> ṃ      (कं -> kaṃ)
ः  -> ḥ      (कः -> kaḥ)

## 4. Special Conjuncts
क्ष -> kṣ
ज्ञ -> jñ
त्र -> tr
श्र -> śr

---

### 3. Reverse Mapping Rules (Roman -> Marathi)

When converting Roman to Devanagari:

- Recognize digraphs: kh, gh, ch, jh, ṭh, ḍh, th, dh, ph, bh.
- Recognize clusters: kṣ, jñ, tr, śr.
- Treat ā, ī, ū, ṇ, ṭ, ḍ, ś, ṣ as atomic phonemes.
- Default inherent vowel = अ when consonant appears without vowel marker.
- If multiple valid spellings exist, ask for clarification instead of guessing.

---

### 4. Preserve Structure

- Preserve punctuation exactly.
- Preserve spacing.
- Do not alter capitalization except where required by script rules.
- Do not add or remove words.
- Never replace Roman words with Marathi synonyms.
- Never correct grammar.
- Never change word order.

---

## Validation Rules

Before returning output:

- Ensure no orphaned matras.
- Ensure conjuncts are valid Devanagari combinations.
- Ensure Roman output uses correct diacritics.
- If input is malformed, request correction.

---

## Examples

### Marathi -> Roman

मराठी भाषा सुंदर आहे -> marāṭhī bhāṣā sundar āhe.

---

### Roman -> Marathi

majhā nāv ānand āhe -> माझा नाव आनंद आहे

---

### Conjunct Handling

क्षत्रिय -> kṣatriya

---

## Enforcement Principle

This skill performs deterministic script conversion.

Allowed:
मराठी -> marāṭhī
bhāṣā -> भाषा

NOT ALLOWED:
hello -> नमस्कार
good morning -> शुभ सकाळ

If the input appears to be English language text instead of Romanized Marathi, ask the user to confirm.

---