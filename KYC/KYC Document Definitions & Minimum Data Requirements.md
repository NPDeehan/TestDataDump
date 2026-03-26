# KYC Document Definitions & Minimum Data Requirements

### Financial Institution — Document Specification Standard

---

## Overview

This document defines each document type accepted or required during the KYC onboarding process. For each document type, a formal definition is provided alongside the minimum data fields that must be present and legible for the document to be considered valid by the KYC validation agent.

---

## 1\. Government-Issued Photo ID

**Definition:** An official identity document issued by a national or regional government authority that includes a photograph of the bearer. It serves as the primary means of confirming a customer's legal identity and is mandatory for all applicants.

**Accepted Forms:**

- Passport  
- National Identity Card  
- Driver's Licence

**Minimum Required Data:**

| Field | Description |
| :---- | :---- |
| Full Legal Name | First name and surname as registered with the issuing authority |
| Date of Birth | In a clearly readable format (DD/MM/YYYY or equivalent) |
| Document Number | Unique alphanumeric identifier assigned by the issuing authority |
| Issuing Country | The country or authority responsible for issuing the document |
| Expiry Date | Must be a future date at the time of application |
| Photograph | A clear, unobstructed facial photograph of the bearer |
| Signature | Bearer's signature (where applicable to document type) |
| MRZ / Barcode | Machine-readable zone or barcode where present (used for authenticity validation) |

**Validation Notes:**

- The document must show no signs of tampering, alteration, or damage to critical data fields.  
- The photograph must be of sufficient quality to perform a visual or automated facial comparison.  
- Expired documents are rejected outright per requirement 1.1.2.

---

## 2\. Proof of Residential Address

**Definition:** A document issued by a recognised third-party institution that confirms the customer's current physical place of residence. It must be recent to ensure the address is current and accurate.

**Accepted Forms:**

- Utility bill (electricity, gas, water, internet)  
- Bank or building society statement  
- Government-issued letter or tax notice  
- Mortgage or tenancy agreement (where dated within the validity window)

**Minimum Required Data:**

| Field | Description |
| :---- | :---- |
| Full Name | Must match the name on the submitted photo ID |
| Residential Address | Full address including street, city, postcode, and country |
| Issue Date | Date the document was issued or the statement period end date |
| Issuing Organisation | Name of the utility provider, bank, or government body |
| Account or Reference Number | Identifier linking the document to the customer (e.g., account number) |

**Validation Notes:**

- For SAVINGS accounts: document must be dated within the last **90 days** (requirement 2.1.1.2).  
- For PERSONAL accounts: document must be dated within the last **60 days** (requirement 2.2.1.3).  
- PO Box addresses are not acceptable as a sole proof of residence.  
- Handwritten documents are not accepted.

---

## 3\. Certificate of Incorporation

**Definition:** An official legal document issued by the relevant companies registrar or government authority confirming that a legal entity has been formally registered and exists as a recognised corporate body. Required for all CORPORATE account applicants.

**Accepted Forms:**

- Certificate of Incorporation  
- Certificate of Registration  
- Articles of Association (where serving as the primary registration document)

**Minimum Required Data:**

| Field | Description |
| :---- | :---- |
| Registered Legal Name | Full legal name of the entity exactly as registered |
| Company Registration Number | Unique identifier assigned by the registrar |
| Date of Incorporation | The date the entity was legally formed |
| Jurisdiction of Incorporation | Country or state in which the entity is registered |
| Registered Office Address | The entity's official legal address |
| Company Type | Legal structure (e.g., Ltd, PLC, LLC, GmbH, partnership) |
| Issuing Authority | Name of the registrar or government body that issued the document |
| Official Seal or Signature | Authentication mark from the issuing authority |

**Validation Notes:**

- The entity must be currently active; dissolved or struck-off entities are rejected.  
- Documents must be an official original or certified copy; scanned photocopies are accepted only if notarised.  
- Entities incorporated in FATF grey/black list jurisdictions trigger mandatory EDD per requirement 2.3.2.4.

---

## 4\. Audited / Management Accounts

**Definition:** Financial statements that summarise the economic activity and financial position of a legal entity over a defined reporting period. These are used to assess the financial legitimacy, scale, and risk profile of a CORPORATE applicant.

**Accepted Forms:**

- Audited annual financial statements (preferred)  
- Management accounts (accepted where audited accounts are unavailable)  
- Abbreviated accounts filed with a companies registrar

**Minimum Required Data:**

| Field | Description |
| :---- | :---- |
| Entity Name | Must match the name on the Certificate of Incorporation |
| Reporting Period | Start and end date of the financial period covered |
| Balance Sheet | Summary of assets, liabilities, and equity |
| Profit & Loss Statement | Income, expenditure, and net profit or loss for the period |
| Turnover / Revenue | Total revenue generated during the period |
| Auditor Name & Signature | Name and signature of the independent auditor (for audited accounts) |
| Auditor's Opinion | Statement of whether the accounts present a true and fair view |
| Date of Approval | Date the accounts were formally approved by directors or management |

**Validation Notes:**

- Accounts must cover the most recently completed financial year.  
- Management accounts are acceptable only where audited accounts are not yet available (e.g., newly incorporated entities).  
- Accounts showing insolvency, significant liabilities, or unexplained financial anomalies must be flagged for compliance review.

---

## 5\. UBO Identity Document

**Definition:** A government-issued identity document submitted on behalf of each Ultimate Beneficial Owner (UBO) — any natural person holding 25% or greater ownership or control of a CORPORATE applicant. These documents establish the identity of the individuals who ultimately own or control the entity.

**Accepted Forms:**

- Passport (preferred)  
- National Identity Card  
- Driver's Licence

**Minimum Required Data:**

| Field | Description |
| :---- | :---- |
| Full Legal Name | First name and surname of the UBO |
| Date of Birth | Must be clearly legible |
| Document Number | Unique identifier on the identity document |
| Issuing Country | Country that issued the document |
| Expiry Date | Must be a future date at the time of application |
| Photograph | Clear facial photograph of the UBO |
| Ownership Percentage | Declared percentage of ownership or control (must be 25% or greater) |

**Validation Notes:**

- All UBOs holding 25% or greater must be declared per requirement 2.3.1.5.  
- UBOs holding 50% or greater must provide a verified photo ID per requirement 2.3.2.2.  
- Each UBO must individually pass sanctions screening per requirement 2.3.2.1.  
- Any UBO identified as a PEP triggers EDD per requirement 2.3.2.7.

---

## 6\. Proof of Income

**Definition:** A document issued by an employer, tax authority, or financial institution that formally evidences a customer's declared income or financial means. Required when a customer's declared transaction volumes exceed defined risk thresholds.

**Accepted Forms:**

- Recent payslip (employed individuals)  
- Tax return or tax assessment notice (self-employed or high earners)  
- Pension statement or letter  
- Employment contract specifying salary (supplementary only)

**Minimum Required Data:**

| Field | Description |
| :---- | :---- |
| Full Name | Must match the name on the primary photo ID |
| Income Amount | Gross or net income clearly stated for the period |
| Pay Period | The period to which the income relates (e.g., monthly, annual) |
| Employer or Issuing Body | Name of the employer, tax authority, or pension provider |
| Issue Date | Date the document was produced |
| Tax Reference or Employee Number | Identifier linking the document to the individual |

**Validation Notes:**

- Required for SAVINGS applicants with expected monthly deposits exceeding **€10,000** (requirement 2.1.2.1).  
- Required for PERSONAL applicants with expected monthly transactions exceeding **€25,000** (requirement 2.2.2.2).  
- Payslips must be dated within the last **90 days**.  
- Tax returns must be the most recently filed return.

---

## 7\. Proof of Business Activity

**Definition:** A document that confirms a self-employed individual or sole trader is engaged in a legitimate and verifiable commercial activity. Required for PERSONAL account applicants who declare self-employment as their employment status.

**Accepted Forms:**

- Business registration certificate  
- VAT registration certificate  
- Tax authority confirmation of self-employment status  
- Most recent filed business tax return

**Minimum Required Data:**

| Field | Description |
| :---- | :---- |
| Full Legal Name or Trading Name | Name of the individual or business as registered |
| Business Registration Number | Unique identifier assigned by the registrar or tax authority |
| Nature of Business Activity | Description of the goods or services provided |
| Registration Date | Date the business was registered |
| Issuing Authority | Name of the registrar or tax authority |
| Business Address | Registered or principal place of business |

**Validation Notes:**

- Required per requirement 2.2.2.1 for all self-employed PERSONAL account applicants.  
- The business activity declared must be consistent with the financial profile provided.  
- Dissolved or deregistered businesses are not accepted.

---

## 8\. Notarised / Apostilled Identity Document

**Definition:** A certified copy of a primary identity document that has been authenticated by a notary public or bears an apostille stamp, confirming its authenticity for cross-border or high-risk verification purposes. Required where standard document validation is insufficient.

**Accepted Forms:**

- Notarised copy of passport  
- Notarised copy of national identity card  
- Apostilled copy of any accepted photo ID

**Minimum Required Data:**

| Field | Description |
| :---- | :---- |
| All fields from the underlying photo ID | As specified in Section 1 of this document |
| Notary Full Name | Name of the certifying notary public |
| Notary Signature & Seal | Official signature and stamp of the notary |
| Date of Notarisation | Date on which the notary certified the document |
| Apostille Reference (if applicable) | Reference number of the apostille stamp |
| Issuing Competent Authority (if apostilled) | The authority that issued the apostille |

**Validation Notes:**

- Required for non-resident PERSONAL account applicants per requirement 2.2.2.6.  
- Required for all Enhanced Due Diligence cases per requirement 4.3.  
- The date of notarisation must be within the last **6 months**.  
- Documents must be notarised in the country of issuance or the applicant's country of residence.

---

## 9\. Commercial Supporting Documentation

**Definition:** Business documents that evidence the legitimate commercial basis for high-volume transactional activity declared by a CORPORATE applicant. Required where expected monthly transaction volumes exceed the defined threshold.

**Accepted Forms:**

- Signed commercial contracts with counterparties  
- Invoices or purchase orders  
- Trade agreements or framework agreements  
- Letters of credit or supplier agreements

**Minimum Required Data:**

| Field | Description |
| :---- | :---- |
| Entity Name | Must match the name on the Certificate of Incorporation |
| Counterparty Name | Name of the business or individual the entity transacts with |
| Nature of Transaction | Description of the goods, services, or activity being transacted |
| Transaction Value or Volume | Monetary amounts and/or frequency of transactions |
| Contract or Invoice Date | Date of the agreement or invoice |
| Signatures of Both Parties | Signed by authorised representatives of each party |
| Counterparty Jurisdiction | Country where the counterparty is located |

**Validation Notes:**

- Required for CORPORATE applicants with expected monthly volumes exceeding **€100,000** per requirement 2.3.2.6.  
- Documents must be current and relate to ongoing or recently completed activity.  
- Counterparty jurisdictions are assessed for sanctions and high-risk country exposure.

---

## 10\. Enhanced Source-of-Funds Declaration

**Definition:** A formal written declaration, supported by documentary evidence, that explains the origin of the funds a customer intends to deposit or transact with. Required for all Enhanced Due Diligence cases.

**Accepted Forms:**

- Signed declaration form accompanied by supporting evidence such as:  
  - Sale of property or asset (conveyancing documents, sale agreement)  
  - Inheritance (grant of probate, will extract)  
  - Business income (company accounts, dividend records)  
  - Investment proceeds (brokerage statements)

**Minimum Required Data:**

| Field | Description |
| :---- | :---- |
| Full Name of Declarant | Must match primary ID |
| Source Description | Clear narrative explanation of where the funds originated |
| Amount | Total value of funds being declared |
| Date of Receipt | When the funds were received or became available |
| Supporting Evidence Reference | Reference to the attached corroborating document(s) |
| Declarant Signature | Signed by the customer or authorised representative |
| Date of Declaration | Date the declaration was completed |

**Validation Notes:**

- Required for all EDD cases per requirement 4.1.  
- The declaration alone is insufficient; supporting documentary evidence must accompany it.  
- Inconsistencies between the declaration and supporting documents must be escalated.

---

## 11\. Enhanced Source-of-Wealth Declaration

**Definition:** A formal written declaration that explains how a customer has accumulated their overall net worth or asset base over time, as distinct from the immediate source of funds. Required for all Enhanced Due Diligence cases.

**Accepted Forms:**

- Signed declaration form accompanied by supporting evidence such as:  
  - Employment history and salary records  
  - Business ownership and sale documents  
  - Inheritance or gift documentation  
  - Investment and savings history

**Minimum Required Data:**

| Field | Description |
| :---- | :---- |
| Full Name of Declarant | Must match primary ID |
| Wealth Narrative | Explanation of how overall wealth was accumulated over time |
| Estimated Net Worth | Approximate total asset value |
| Key Wealth Events | Significant events contributing to wealth (e.g., business sale, inheritance) |
| Timeline | Approximate dates of major wealth accumulation events |
| Supporting Evidence Reference | Reference to the attached corroborating document(s) |
| Declarant Signature | Signed by the customer or authorised representative |
| Date of Declaration | Date the declaration was completed |

**Validation Notes:**

- Required for all EDD cases per requirement 4.2.  
- Must be reviewed alongside the Source-of-Funds Declaration for consistency.  
- Gaps or implausibilities in the wealth narrative must be escalated to a compliance officer.

---

*Document Version: 1.0 | Classification: Internal — Compliance Use* *Cross-reference: KYC Validation Procedures & Requirements v1.0*

