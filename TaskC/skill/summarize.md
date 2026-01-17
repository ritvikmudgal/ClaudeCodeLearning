# Skill: doc_summarize
## Purpose
Convert long-form technical specs into requirement bullet points.

## Inputs
- document_text: string

## Outputs
- requirements: list of bullet points

## Tools Used
- None

## Steps / Algorithm
1. Segment text by headings or paragraphs.
2. Extract requirement-like sentences ("must", "shall", "should").
3. Normalize text to bullet points.
4. Remove duplicates.

## Failure Modes
- Non-technical text → may produce generic bullets.
- Missing input → return error message.

## Test Cases
### Test 1
Input: "System shall log errors."
Output: ["System shall log errors"]
### Test 2
Input: ""
Output: error: no document provided
