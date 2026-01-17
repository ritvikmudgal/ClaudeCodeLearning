# Workflow Execution Trace (7 Steps)

**Example:**  
User asks → *“Summarize this spec and prioritize tasks.”*

---

## 1. User Intent Received
**Input:**  
- Document text  
- Tasks

---

## 2. Engine Interprets Intent
- Extracts dual objectives:
  - Summarize
  - Triage

---

## 3. Engine Routes to Skills
- `doc_summarize` for summarization  
- `triage` for prioritization

---

## 4. Engine Executes `doc_summarize`
- Returns requirements list

---

## 5. Engine Executes `triage`
- Returns prioritized tasks

---

## 6. Engine Validates Outputs
- Checks formatting consistency  
- Checks for missing fields

---

## 7. Engine Returns Final Output
- Merged and formatted for user consumption
