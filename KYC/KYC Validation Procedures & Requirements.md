# KYC Validation Procedures & Requirements

### Financial Institution — Customer Onboarding Standard

---

## Overview

This document defines the procedures and requirements for validating whether a financial institution may onboard a new customer. It is structured for use by an automated KYC validation agent with the following capabilities:

- **Record Lookup** — Query existing internal customer and account records  
- **Account Data Check** — Review linked financial account history and status  
- **Sanctions Screening** — Cross-reference customer data against sanctions and watchlists  
- **Document Validation** — Verify authenticity and integrity of submitted identity documents  
- **Additional Documentation Requests** — Prompt the customer to submit supplementary evidence where required

All requirements are numbered within their sections for precise reference during automated decision-making.

---

## Section 1 — Universal Basic Requirements

These checks apply to **all** customers, regardless of account type requested.

### 1.1 Identity Submission

1.1.1 — The customer must submit a valid government-issued photo ID (passport, national ID card, or driver's licence).  
1.1.2 — The submitted ID must not be expired at the time of application.  
1.1.3 — The ID must contain a full legal name, date of birth, and a unique identifier (document number).  
1.1.4 — The agent must perform document validation to confirm the ID is unaltered and authentic.  
1.1.5 — The name on the ID must exactly match the name provided in the application form (allowing for minor transliteration differences).

### 1.2 Basic Biographical Checks

1.2.1 — The customer's date of birth must confirm they are at minimum **18 years of age**.  
1.2.2 — The customer must provide a declared country of residence.  
1.2.3 — The customer must provide a contact address (physical or registered).  
1.2.4 — A valid email address and phone number must be collected for contact verification.

### 1.3 Existing Record Lookup

1.3.1 — The agent must query internal records to determine whether the customer already holds an account.  
1.3.2 — If an existing record is found, the agent must verify the submitted ID matches the record on file.  
1.3.3 — If the existing record shows a previously rejected or flagged application, escalation is required before proceeding.  
1.3.4 — If the existing record shows an active account in good standing, identity re-verification may be streamlined per Section 3\.

### 1.4 Sanctions Screening

1.4.1 — The customer's full legal name and date of birth must be screened against all applicable sanctions lists (e.g., OFAC SDN, EU Consolidated List, UN Sanctions List).  
1.4.2 — The customer's declared country of residence must not appear on restricted or embargoed country lists.  
1.4.3 — Any fuzzy match (≥ 85% name similarity) against a sanctions record must be flagged for human review before proceeding.  
1.4.4 — A confirmed sanctions match must result in immediate rejection of the application.

### 1.5 Basic Financial Information

1.5.1 — The customer must declare their primary source of income or funds.  
1.5.2 — The customer must declare their estimated monthly transaction volume.  
1.5.3 — The customer must declare their occupation or business activity.  
1.5.4 — Declared financial information must be assessed for internal consistency and plausibility against the account type requested.

---

## Section 2 — Account-Type Specific Requirements

### 2.1 SAVINGS Account

*Intended for individuals seeking a standard deposit and savings facility.*

#### 2.1.1 Basic Requirements

2.1.1.1 — The applicant must be an individual (natural person); entities are not eligible for a SAVINGS account.  
2.1.1.2 — Proof of a residential address must be provided (e.g., utility bill or bank statement dated within 90 days).  
2.1.1.3 — The declared source of funds must be consistent with an individual income source (e.g., employment, pension, self-employment).  
2.1.1.4 — Expected monthly deposit volume must be declared and must not exceed a low-to-moderate risk threshold without additional verification.

#### 2.1.2 Advanced Requirements

2.1.2.1 — If the expected monthly deposit volume exceeds **€10,000**, proof of income (e.g., payslip, tax return) must be requested as additional documentation.  
2.1.2.2 — Customers from high-risk jurisdictions (as defined by FATF) must undergo enhanced due diligence (EDD) — see Section 4\.  
2.1.2.3 — If no existing record is found and the ID cannot be verified through document validation, a secondary form of ID must be requested.  
2.1.2.4 — Politically Exposed Persons (PEPs) applying for a SAVINGS account require senior approval and enhanced monitoring.

---

### 2.2 PERSONAL Account

*Intended for individuals seeking a full-service transactional and current account.*

#### 2.2.1 Basic Requirements

2.2.1.1 — The applicant must be an individual (natural person).  
2.2.1.2 — A valid photo ID satisfying all Section 1.1 requirements must be submitted.  
2.2.1.3 — Proof of residential address dated within **60 days** must be submitted.  
2.2.1.4 — Employment status must be declared (employed, self-employed, unemployed, student, retired).  
2.2.1.5 — Estimated monthly incoming and outgoing transaction volumes must be declared.

#### 2.2.2 Advanced Requirements

2.2.2.1 — If the applicant is self-employed, they must submit proof of business activity (e.g., business registration or tax certificate).  
2.2.2.2 — If the declared monthly transaction volume exceeds **€25,000**, proof of income source must be requested as additional documentation.  
2.2.2.3 — If account data checks reveal prior negative financial behaviour (e.g., defaults, closures for misconduct) at another institution accessible in the record, the application must be escalated.  
2.2.2.4 — The customer must not appear as a beneficial owner of a sanctioned entity identified during sanctions screening.  
2.2.2.5 — PEP status must be assessed; confirmed PEPs require an enhanced due diligence pathway (Section 4).  
2.2.2.6 — Where the customer is a non-resident, a notarised copy of the ID document must be requested as additional documentation.

---

### 2.3 CORPORATE Account

*Intended for legal entities such as companies, partnerships, and other registered organisations.*

#### 2.3.1 Basic Requirements

2.3.1.1 — The applicant must be a registered legal entity with a valid company registration number.  
2.3.1.2 — A certificate of incorporation or equivalent registration document must be submitted and validated.  
2.3.1.3 — The entity's registered business address must be provided and verified.  
2.3.1.4 — The entity's primary business activity (industry/sector) must be declared.  
2.3.1.5 — The full legal names and dates of birth of all **Ultimate Beneficial Owners (UBOs)** holding ≥ 25% ownership must be declared.  
2.3.1.6 — At least one authorised signatory must be identified and their identity verified per Section 1.1.  
2.3.1.7 — The entity must submit its most recent set of audited or management accounts.

#### 2.3.2 Advanced Requirements

2.3.2.1 — All declared UBOs must individually pass sanctions screening per Section 1.4.  
2.3.2.2 — All UBOs must be identity-verified; those holding ≥ 50% must provide a verified photo ID per Section 1.1.  
2.3.2.3 — If the entity operates in a high-risk industry (e.g., gambling, crypto-assets, arms, money services), enhanced due diligence is mandatory per Section 4\.  
2.3.2.4 — If the entity is incorporated in a high-risk or non-cooperative jurisdiction (FATF grey/black list), enhanced due diligence is mandatory per Section 4\.  
2.3.2.5 — The entity's ownership structure must be fully documented; complex multi-layered structures must be mapped and reviewed by a compliance officer.  
2.3.2.6 — Expected transaction volumes and counterparty jurisdictions must be declared; volumes exceeding **€100,000/month** require supporting commercial documentation (e.g., contracts, invoices).  
2.3.2.7 — Any UBO identified as a PEP triggers mandatory enhanced due diligence per Section 4\.  
2.3.2.8 — Shell companies or entities with no apparent commercial activity must be escalated for review and are presumptively rejected unless a legitimate purpose is demonstrated.

---

## Section 3 — Existing Customer Streamlining

3.1 — If the customer holds an existing account in good standing and their identity has been verified within the last **24 months**, full document re-validation may be waived.  
3.2 — Sanctions screening must always be re-run regardless of existing customer status.  
3.3 — Account-type specific requirements (Section 2\) remain fully applicable for each new account type requested.  
3.4 — If any previously submitted documentation has expired (e.g., ID, proof of address), it must be re-requested before proceeding.  
3.5 — A risk re-assessment must be triggered if the customer's declared financial profile has changed materially since last onboarding.

---

## Section 4 — Enhanced Due Diligence (EDD)

EDD is triggered by flags raised in Sections 1–3. All EDD cases must be reviewed by a compliance officer before a final decision is issued.

4.1 — The customer or entity must provide an enhanced source-of-funds declaration with supporting documentary evidence.  
4.2 — The customer or entity must provide an enhanced source-of-wealth declaration explaining the accumulation of assets.  
4.3 — Additional proof of address and identity documentation must be requested, including notarised or apostilled copies where applicable.  
4.4 — For corporate accounts, a full UBO ownership chain must be documented to the level of natural persons.  
4.5 — Ongoing transaction monitoring must be set to a heightened frequency for any account that passes EDD.  
4.6 — EDD reviews must be repeated on a **12-month cycle** for as long as the elevated risk classification persists.  
4.7 — The final EDD approval must be signed off by a designated senior compliance officer; automated approval is not permitted.

---

## Section 5 — Decision Outcomes

| Code | Outcome | Condition |
| :---- | :---- | :---- |
| `APPROVED` | Application approved | All applicable requirements met, no flags |
| `PENDING_DOCS` | Awaiting additional documentation | Agent has requested supplementary materials |
| `PENDING_EDD` | Awaiting enhanced due diligence review | EDD triggered; pending compliance officer review |
| `ESCALATED` | Referred to human review | Ambiguous match, conflicting data, or policy edge case |
| `REJECTED` | Application rejected | Confirmed sanctions match, fraudulent document, or unresolvable risk |

---

## Section 6 — Agent Behaviour Rules

6.1 — The agent must not approve an application without completing all mandatory checks for the relevant account type(s).  
6.2 — Where a customer has applied for multiple account types simultaneously, the most stringent applicable requirements govern.  
6.3 — The agent may request additional documentation a maximum of **two times** before escalating to human review.  
6.4 — All agent decisions must be logged with a reference to the specific requirement(s) that informed the outcome.  
6.5 — The agent must never store raw ID document images beyond the validation step; only the validation result and document metadata may be retained.  
6.6 — Any system error or data unavailability during a mandatory check must result in a `PENDING` status and human review, never a default approval.

---

*Document Version: 1.0 | Classification: Internal — Compliance Use*

*Written with Glean Assistant*  
