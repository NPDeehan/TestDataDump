# KYC Validation Procedure Requirements (Demo Version)

### Financial Institution - Simplified AI Decision Paths

---

## 1. Purpose

This document defines simple and clear validation flows for a demo AI agent.

This procedure applies to all new customers and to any existing customer who does not hold an L1 trust level. A risk check must be completed for all such customers before any application can proceed.

All potential clients are assigned a default trust level of **L3** unless an existing record on file explicitly states otherwise.

The available tools stay the same:

- Record Lookup
- Account Data Check
- Sanctions Screening
- Document Validation
- Additional Documentation Requests

---

## 2. Universal Checks (Apply to Every Application)

2.1 Customer must be 18 or older.  
2.2 Name and date of birth must be present and consistent across application and ID.  
2.3 Sanctions screening must run for every application against the applicant's employer and any associated companies only. Sanctions screening is not applied to individual persons.  
2.4 Confirmed sanctions match against an employer or associated company = immediate rejection.  
2.5 If any mandatory check cannot run (tool/data unavailable), return ESCALATED.

---

## 3. Demo Decision Paths

### 3.1 Path A - Credit Card (Existing Customer, Easy Path)

Use this path when customer already has an active account.

3.1.1 Record Lookup must confirm customer exists.  
3.1.2 Account Data Check must show account status is good standing (not blocked, not delinquent).  
3.1.3 Available balance must be greater than 1000.  
3.1.4 Sanctions screening of the applicant's employer and any associated companies must be clear.

If all conditions 3.1.1 to 3.1.4 are true: outcome = APPROVED (auto-approved credit card).  
If customer exists but balance is 1000 or less: route to Path B document-based review.  
If good standing cannot be confirmed: outcome = ESCALATED.

### 3.2 Path B - Personal Account Opening (Light KYC)

Required documents:

- Government ID
- Proof of address (dated within 90 days)

3.2.1 Validate ID authenticity and expiry.  
3.2.2 Validate proof of address authenticity and recency.  
3.2.3 Name on ID must match application name (allow minor formatting differences).  
3.2.4 Sanctions screening of the applicant's employer and any associated companies must be clear.

If all required documents are valid and checks pass: outcome = APPROVED.  
If one or more required documents are missing/invalid: outcome = PENDING_DOCS.

### 3.3 Path C - Insurance Application (Higher Documentation)

Required documents:

- Government ID
- Proof of address (dated within 90 days)
- Proof of employment (or equivalent proof of income)

3.3.1 Complete all checks from Path B.  
3.3.2 Validate employment/income document authenticity and relevance.  
3.3.3 If employment or income cannot be reasonably validated: outcome = ESCALATED.

If all three documents are valid and employer/company sanctions check is clear: outcome = APPROVED.  
If required documents are missing: outcome = PENDING_DOCS.

---

## 4. Decision Outcomes

| Code | Outcome | Condition |
| :---- | :---- | :---- |
| APPROVED | Application approved | All required checks for selected path pass |
| PENDING_DOCS | Awaiting customer documents | Missing or invalid mandatory document(s) |
| ESCALATED | Human review required | Tool/data unavailable, ambiguous result, or risk flag |
| REJECTED | Application rejected | Confirmed sanctions match or confirmed document fraud |

---

## 5. Agent Behavior Rules (Simplified)

5.1 Agent must select one path only (A, B, or C) based on product requested and existing customer status.  
5.2 Agent may request additional documents a maximum of two times before ESCALATED.  
5.3 Every outcome must log the rule numbers used.  
5.4 Agent must never default to approval if a required check fails or cannot run.

---

## 6. Document File References for Validation

- govID.md
- proofAddress.md
- proofOfIncome.md

Optional references for fallback/escalation scenarios:

- sourceOfFunds.md
- sourceOfWealth.md
- noterizedDocument.md

---

*Document Version: 2.0 (Demo Simplified)*
