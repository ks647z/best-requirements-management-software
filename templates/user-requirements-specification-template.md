# User Requirements Specification (URS) template

A URS skeleton with an identifier scheme, acceptance criteria and a verification method against every requirement. Copy it, fill it, and move it into a tool before it reaches version 7.

Licensed CC BY 4.0 by [Matrix One](https://matrixone.health). Attribution appreciated, not policed.

---

## 1. Document control

| Field | Value |
|-------|-------|
| Document ID | URS-001 |
| Version | 0.1 |
| Status | Draft / In review / Approved |
| Author | |
| Reviewer | |
| Approver | |
| Approval date | |
| Supersedes | |

**Change history**

| Version | Date | Author | Change | Change request |
|---------|------|--------|--------|----------------|
| 0.1 | | | Initial draft | |

## 2. Scope

What product, which release, which markets, and what is explicitly out of scope. Out of scope is the more useful half and the half most teams skip.

## 3. Definitions and identifier scheme

Agree this before you write requirement one. Renumbering later is painful in every tool.

| Prefix | Meaning | Example |
|--------|---------|---------|
| UN | User need | UN-001 |
| SYS | System requirement | SYS-001 |
| SWR | Software requirement | SWR-001 |
| HWR | Hardware requirement | HWR-001 |
| RSK | Risk | RSK-001 |
| RC | Risk control | RC-001a |
| TC | Test case | TC-001 |

Identifiers are never reused and never renumbered. A deleted requirement is marked obsolete, not removed.

## 4. Stakeholders and intended use

Who uses the product, in what environment, with what training assumed. For a medical device this is where the intended use statement and the user profile live, and everything downstream is traced back to it.

## 5. Regulatory and standards context

List the standards the product is developed against, so the requirements can be traced to them.

- ISO 13485 quality management systems
- IEC 62304 medical device software life cycle
- ISO 14971 risk management
- FDA 21 CFR Part 820 (QMSR, in force from 2 February 2026, incorporating ISO 13485 by reference)
- EU MDR 2017/745
- IEC 62366 usability engineering

## 6. User requirements

One requirement per row. One requirement per requirement: if the text contains "and", check whether it is really two.

| ID | Requirement | Rationale | Priority | Acceptance criteria | Verification method | Traces to | Status |
|----|-------------|-----------|----------|---------------------|---------------------|-----------|--------|
| UN-001 | The user shall be alerted when the reservoir falls below 10 percent capacity. | Interrupted therapy risk | Must | Alert is perceived by 95 percent of participants in formative usability testing within 5 seconds | Validation | RSK-012 | Draft |
| UN-002 | | | | | | | |

**Verification method** is one of: Test, Inspection, Analysis, Demonstration, Validation. If you cannot name one, the requirement is not testable and is not yet a requirement.

## 7. Non functional requirements

Performance, reliability, security, cybersecurity, data retention, interoperability, localisation, accessibility. Same table shape as section 6. These are the requirements most often written as adjectives, and an adjective cannot be verified. Put a number on each one.

## 8. Constraints and assumptions

Anything the design must accept as fixed, and anything you are assuming that a later reader should be able to challenge.

## 9. Traceability

Every user requirement traces forward to at least one system requirement and at least one verification, and backward to a stakeholder need or a regulatory clause. Anything with no trace in either direction is either scope creep or a gap, and both are worth finding now.

Use [`traceability-matrix-template.csv`](traceability-matrix-template.csv) while this lives in files, and generate it once it lives in a tool.

## 10. Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Author | | | |
| Reviewer | | | |
| Quality | | | |
| Approver | | | |
