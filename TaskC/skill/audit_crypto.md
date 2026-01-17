# Skill: audit_crypto
## Purpose
Scan config/code snippets for insecure cryptographic patterns.

## Inputs
- code_snippet: string

## Outputs
- findings: list of {issue, severity, recommendation}

## Tools Used
- regex scanning (optional)

## Steps / Algorithm
1. Scan for weak algorithms (MD5, SHA1).
2. Scan for static IV/keys.
3. Scan for ECB mode usage.
4. For each finding, attach severity.
5. Generate recommendations.
6. Return findings.

## Failure Modes
- False positives if variable names contain crypto terms.
- No crypto found → return empty findings.

## Test Cases
### Test 1
Input: "hash = md5(data)"
Output: finding: MD5 detected → severity: high
### Test 2
Input: "hash = sha256(data)"
Output: findings = []
