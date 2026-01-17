# Skill: triage
## Purpose
Analyze a list of issues or tasks and classify them by priority and recommended remediation.

## Inputs
- issues: list of {title, description, severity}

## Outputs
- prioritized list with fields:
  {priority, remediation_plan, justification}

## Tools Used
- None (pure reasoning)

## Steps / Algorithm
1. Parse issue metadata.
2. Assign priority (P1/P2/P3) based on severity keywords.
3. Generate remediation plan (short actionable steps).
4. Justify prioritization with 1-2 sentences.
5. Return structured output.

## Failure Modes & Mitigation
- Missing severity → default to P3 and flag missing data.
- Empty input → return "No issues provided."

## Test Cases
### Test Case 1
Input: [{severity: "high"}]
Output: first issue tagged P1 + remediation
### Test Case 2
Input: []
Output: "No issues provided."
