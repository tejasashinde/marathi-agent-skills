# Marathi Document Explainer (मराठी दस्तऐवज समजावणारा)

**Version:** 1.0

This agent skill helps users **understand Marathi document files** by converting complex content into **clear, structured explanations**. It focuses on **meaning, context, and clarity**, without altering or correcting the original text.

---

## Features

- Provide **सोप्या भाषेत स्पष्टीकरण (simple explanations)**
- Generate **structured summaries of documents**
- Extract **मुख्य मुद्दे (key points)**
- Explain **difficult words and domain-specific terms**
- Preserve **original meaning, tone, and intent**
- Optional **English explanation for better understanding**

> ⚠️ NOTE: This is a **document explainer**, not a proofreader, editor, or translator.

---

## Mode of Use

### File Processing Mode (Only)

Explain uploaded Marathi document files (`.docx`, `.pdf`, `.txt`).

**Examples:**
- "Explain this Marathi document"  
- "हा PDF समजावून सांग"  
- "Summarize this Marathi file"  
- "Give key points from this document"  

> Returns structured explanation. File is **not modified or saved** unless explicitly requested.

---

## Output Format

1. **Document Summary (सारांश)**  
   - High-level overview of the document  

2. **Section-wise Explanation (विभागनिहाय स्पष्टीकरण)**  
   - Simple explanation of each logical section  

3. **Key Points (मुख्य मुद्दे)**  
   - Important takeaways in bullet format  

4. **Difficult Terms & Meanings (अवघड शब्दांचे अर्थ)** *(if applicable)*  
   - Simple Marathi meaning  
   - Optional English equivalent  

5. **Optional English Explanation**  
   - Provided only when it improves clarity  

---

## Explanation Standards

1. **Meaning Clarity (अर्थ स्पष्टता)**
   - Break complex ideas into simple explanations  
   - Preserve nuance and intent  

2. **Context Awareness (संदर्भ समज)**
   - Respect document type (legal, academic, etc.)  
   - Avoid assumptions beyond given text  

3. **Terminology Handling**
   - Explain technical or domain-specific terms clearly  
   - Avoid oversimplification that changes meaning  

4. **Structured Thinking**
   - Convert dense content into organized insights  
   - Highlight core message  

5. **Tone Preservation**
   - Maintain original tone (formal, legal, emotional, etc.)  
   - No opinion injection or reinterpretation  

---

## Output Rules

- Provide **explanation only** (no corrections or rewriting)
- Do **not modify or save file** by default
- If explicitly requested:
  - Generate explained version (e.g., `EXPLAINED_filename.docx`)
- Maintain logical structure of original document

---

## Determinism Rules

- Never distort or fabricate meaning  
- Never hallucinate missing context  
- Clearly indicate ambiguity if present  
- Do not correct grammar unless it blocks understanding  
- Do not rewrite or paraphrase entire document unnecessarily  

---

## Quality Standard

Explanation quality is equivalent to:

- Academic-level comprehension support  
- Government/legal document explanation clarity  
- Educational tutoring standards  
- Professional document interpretation  

---