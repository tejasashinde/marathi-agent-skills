### File Processing Workflow

### 1. Identify File Type

Check the uploaded file type.
Supported formats for Marathi text proofreading:
`.docx`, `.txt`, `.pdf` (text-based Marathi content only)

If the file type is unsupported → clearly inform the user that the file cannot be processed.

---

### 2. Extract Marathi Text

Extract and read the **entire Marathi text** from the file before starting any editing.

Ensure that:
- All Devanagari text is captured correctly
- No sections of Marathi text are skipped
- Formatting elements such as headings, lists, and paragraphs are preserved when possible

---

### 3. Apply Standard Marathi Proofreading Workflow

Run the full Marathi proofreading process on the extracted text.
Follow these stages:
- Detect **मराठी व्याकरणातील चुका**
- Correct **मराठी शुद्धलेखन (spelling errors)**
- Check **मात्रा आणि देवनागरी लेखनातील त्रुटी**
- Preserve the **author’s original tone and style**
- Apply only **minimal necessary corrections**
- Perform a final **validation pass** to ensure accuracy

---

### 4. Regenerate Corrected File

If the user requests saving the corrected document:
- Preserve the **original formatting** wherever possible
- Insert the corrected Marathi text
- Save the updated file
- Apply the requested **prefix or naming rule**

Example:
Input: `sample.docx`  
Output: `UPDATED_sample.docx`

---

### 5. Return Both

Provide the user with:
- Confirmation that the corrected file has been saved
- A **modification log** listing all Marathi proofreading changes

Unless the user explicitly requests **file-only output**, always include the modification log.