
# Botium Toys — Compliance Gap Analysis

## 1. Overview

This document analyzes selected security and compliance requirements relevant to Botium Toys.

The analysis compares the available organizational evidence against selected requirements from PCI DSS, GDPR, and SOC-related Trust Services Criteria.

The purpose is to identify compliance gaps, assess potential impacts, and recommend security improvements.

## 2. PCI DSS — Payment Card Data Protection

PCI DSS establishes security requirements for organizations that store, process, or transmit payment card data.

| ID | Requirement | Evidence | Gap | Status |
|---|---|---|---|---|
| PCI-01 | Restrict access to cardholder data to authorized users. | All employees have broad access to internal data, including cardholder information. | Access is not adequately restricted by business need. | Gap Identified |
| PCI-02 | Protect cardholder data in a secure environment. | Cardholder data is not adequately protected through encryption. | Sensitive payment information may be exposed to unauthorized access. | Gap Identified |
| PCI-03 | Implement encryption procedures to protect cardholder data. | Payment card information is not encrypted at rest, in transit, or during processing, according to the case documentation. | Encryption protections are insufficient or absent. | Gap Identified |
| PCI-04 | Implement secure password management policies and procedures. | A password policy exists, but requirements are weak. No centralized password management system is available. | Password controls are insufficient to provide adequate protection. | Gap Identified |

### PCI DSS Assessment

**Result: 0 of 4 requirements assessed as satisfied.**

The main weaknesses involve access control, encryption, and password management.

These gaps increase the risk of unauthorized access to payment card information and potential exposure of cardholder data.

## 3. GDPR — Personal Data Protection

The General Data Protection Regulation (GDPR) establishes requirements for processing and protecting personal data belonging to individuals in the European Union.

| ID | Requirement | Evidence | Gap | Status |
|---|---|---|---|---|
| GDPR-01 | Protect the privacy and security of EU customers' personal data. | Employees have broad access to internal data, including PII and SPII. | Access restrictions and data protection measures are insufficient. | Gap Identified |
| GDPR-02 | Maintain a breach notification process. | The organization has a plan to notify EU customers within 72 hours of a data breach. | The available documentation does not establish whether all GDPR notification obligations are correctly addressed. | Partially Supported |
| GDPR-03 | Maintain appropriate data classification and inventory. | No adequate data classification and inventory process is documented. | The organization lacks sufficient visibility into the personal data it holds. | Gap Identified |
| GDPR-04 | Establish and enforce privacy policies and procedures. | Privacy policies and procedures are developed and applied to document and maintain data. | No specific gap was identified from the available evidence, although operational effectiveness has not been independently verified. | Supported by Available Evidence |

### GDPR Assessment

**Educational checklist result: 2 of 4 requirements marked as satisfied.**

The organization demonstrates some privacy governance practices, but significant weaknesses remain in access control and data management.

**Important legal distinction:** GDPR Article 33 generally requires notification to the competent supervisory authority within 72 hours of becoming aware of a personal data breach, where notification is required. Communication to affected individuals is governed separately by Article 34 and applies when the breach is likely to result in a high risk to their rights and freedoms.

Therefore, a customer notification plan mentioning 72 hours does not, by itself, demonstrate full GDPR compliance.

## 4. SOC 1 / SOC 2 — Control Environment

SOC 1 and SOC 2 are independent attestation reporting frameworks developed by the AICPA.

- SOC 1 focuses on controls relevant to user entities' internal control over financial reporting.
- SOC 2 evaluates controls against applicable Trust Services Criteria, including security, availability, processing integrity, confidentiality, and privacy.

The following assessment uses selected SOC-related control concepts. It is not a formal SOC examination.

| ID | Control Area | Evidence | Gap | Status |
|---|---|---|---|---|
| SOC-01 | User access policies | The organization has policies related to user access, but access restrictions are inadequate. | Policy existence does not demonstrate effective enforcement. | Partially Supported |
| SOC-02 | Confidentiality of sensitive PII and SPII | Sensitive information is broadly accessible and payment card information is not adequately encrypted. | Confidentiality protections are insufficient. | Gap Identified |
| SOC-03 | Data integrity | IT reports that controls supporting data integrity are integrated into the environment. | Independent validation of effectiveness is unavailable. | Supported by Available Evidence |
| SOC-04 | Data availability | IT reports that controls supporting availability are integrated into the environment. However, no backups or disaster recovery plan exist. | Availability controls may be insufficient to recover from major incidents. | Partially Supported (Checklist: Yes) |

### SOC-Related Assessment

**Educational checklist result: 3 of 4 requirements marked as satisfied.**

The available evidence suggests that some control practices exist, but weaknesses in confidentiality, access enforcement, and recovery capabilities remain.

The checklist results should not be interpreted as evidence that Botium Toys would pass a SOC 1 or SOC 2 examination.

## 5. Consolidated Results

| Assessment Area | Satisfied / Supported | Gaps / Not Satisfied | Total |
|---|---:|---:|---:|
| PCI DSS | 0 | 4 | 4 |
| GDPR | 2 | 2 | 4 |
| SOC-related criteria | 3 | 1 | 4 |
| **Total** | **5** | **7** | **12** |

These totals reproduce the educational checklist classifications. Partially supported items are preserved as originally classified by the course where applicable, with additional qualifications documented above.

## 6. Cross-Framework Findings

Several weaknesses affect multiple compliance areas:

### Access Control

Excessive employee privileges affect both payment card protection and personal data confidentiality.

### Data Protection

The absence of adequate encryption increases the risk of exposing sensitive payment and personal information.

### Data Governance

Insufficient data classification and inventory make it harder to identify sensitive assets and apply appropriate protections.

### Business Continuity

The absence of backups and disaster recovery planning threatens the availability and recoverability of business-critical information.

### Control Effectiveness

The existence of policies or technical controls does not necessarily demonstrate that they are properly designed, implemented, monitored, and operating effectively.

## 7. Limitations

This analysis is based on fictional organizational documentation and an educational compliance checklist.

It does not constitute:

- A formal PCI DSS assessment.
- A GDPR legal compliance opinion.
- A SOC 1 or SOC 2 examination.
- An independent audit or penetration test.

All conclusions should be interpreted within the limits of the available evidence.

## 8. Conclusion

The analysis identifies significant gaps in access control, data protection, data governance, and business continuity.

Although some policies and controls are documented, their existence alone does not demonstrate effective protection.

The identified gaps should be prioritized according to business impact and security risk. These results will serve as input for the security findings and remediation roadmap.
