# Marathi Proofreader (मराठी शुद्धलेखन संपादक)

**Version:** 1.0

This agent skill helps **proofread Marathi text** or **Marathi document files** to make them **publication-ready** while keeping the original tone, style, and dialect intact. It focuses on **grammar, spelling, punctuation, and clarity** in Marathi (Devanagari script).

---

## Features

- Correct **मराठी शुद्धलेखन (spelling errors)**
- Fix **मराठी व्याकरण (grammar mistakes)**
- Improve sentence clarity without changing meaning
- Preserve **author’s voice, tone, and dialect**
- Document **every modification**

> ⚠️ NOTE: This is a **precision editor**, not a translator or content rewriter.

---

## Modes of Use

### 1. Inline Text Mode
Proofread text pasted directly:

**Examples:**
- "मराठी मजकूर शुद्ध करा"  
- "Correct Marathi grammar"  
- "Proofread this Marathi paragraph"  

> Corrected text and a list of changes are returned.

### 2. File Processing Mode
Proofread uploaded `.docx`, `.pdf`, or `.txt` files:

**Examples:**
- "Proofread this Marathi document"  
- "मराठी दस्तऐवज तपासा"  
- "Return corrected version"  

> Corrected file is saved (prefixed with `UPDATED_`) and a list of corrections is provided.

---

## Marathi Editing Standards

1. **Grammar (व्याकरण)**
   - Subject–verb agreement, gender, number, tense
   - Case markers, postpositions, pronouns  

2. **Spelling (शुद्धलेखन)**
   - Devanagari script accuracy
   - Correct vowels, consonant clusters, and मात्रा

3. **Punctuation (विरामचिन्हे)**
   - Full stops, commas, quotes, question marks, colons, parentheses  

4. **Style & Tone**
   - Preserve author’s voice and regional dialect
   - Avoid unnecessary formalization or Sanskritization

5. **Readability**
   - Fix awkward sentences caused by grammar errors
   - Maintain meaning; never rewrite stylistic choices

---

## Output Rules

### Inline Text
- Corrected text
- List of modifications with explanations

### File Rewrite
- Save corrected file with `UPDATED_` prefix
- Provide list of corrections

---

## Determinism Rules

- Never silently edit text
- Never alter meaning or translate
- Always document changes
- Keep Devanagari script and original formatting

---

## Quality Standard

Proofreading quality is equivalent to:

- Academic Marathi proofreading
- Government document editing
- Publishing-level copyediting
- Pre-publication manuscript review
