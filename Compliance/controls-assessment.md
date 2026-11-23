
# Botium Toys — Security Controls Assessment

## 1. Assessment Overview

This document evaluates the implementation of 14 administrative, technical, and physical security controls at Botium Toys.

The assessment is based on the documentation provided in the educational case study. It identifies whether each control is implemented and highlights relevant weaknesses.

**Assessment results:**
- Controls assessed: 14
- Implemented: 7
- Not implemented: 7

> Important: An implemented control is not necessarily an effective control. Implementation status and control effectiveness must be evaluated separately.

## 2. Controls Assessment

| ID | Security Control | Status | Assessment |
|---|---|---|---|
| C-01 | Least Privilege | Not Implemented | All employees have broad access to internal data, including sensitive information. |
| C-02 | Disaster Recovery Plan | Not Implemented | No documented disaster recovery plan is available. |
| C-03 | Password Policies | Implemented | A password policy exists, but its requirements are insufficient. |
| C-04 | Separation of Duties | Not Implemented | Responsibilities and access privileges are not adequately separated. |
| C-05 | Firewall | Implemented | A firewall is deployed and its rules are considered adequate. |
| C-06 | Intrusion Detection System (IDS) | Not Implemented | No IDS is deployed to identify potentially malicious activity. |
| C-07 | Data Backups | Not Implemented | No backup process for critical data is established. |
| C-08 | Antivirus Software | Implemented | Antivirus software is installed and regularly monitored by IT. |
| C-09 | Manual Monitoring and Maintenance | Implemented | Manual monitoring and maintenance occur, but lack a regular schedule and clearly defined procedures. |
| C-10 | Encryption | Not Implemented | Payment card information is not encrypted at rest, in transit, or during processing, according to the assessment documentation. |
| C-11 | Password Management System | Not Implemented | No centralized system enforces password requirements. |
| C-12 | Physical Locks | Implemented | Physical locations have sufficient locking mechanisms. |
| C-13 | CCTV | Implemented | Updated CCTV systems are installed and operational. |
| C-14 | Fire Detection and Prevention | Implemented | Fire detection and prevention systems are operational. |

## 3. Key Observations

### Identity and Access Management

The organization lacks effective access restrictions based on job responsibilities.

The absence of least privilege and separation of duties increases the possibility of unauthorized access, misuse of privileges, and exposure of sensitive information.

### Data Protection

Payment card information is not adequately protected through encryption.

This creates a significant confidentiality risk, particularly if unauthorized individuals gain access to systems or storage environments containing payment data.

### Business Continuity

The absence of backup procedures and a disaster recovery plan exposes the organization to data loss and prolonged service disruption.

### Security Monitoring

The organization has firewall and antivirus controls, but no Intrusion Detection System (IDS).

This limits its ability to identify suspicious network activity through dedicated intrusion detection capabilities.

### Physical Security

Physical security controls appear to be established, including locks, CCTV, and fire detection systems.

However, the available documentation does not establish their effectiveness through independent testing.

## 4. Assessment Limitations

This assessment relies exclusively on the information provided in the educational case study.

No independent technical validation, penetration testing, configuration review, or physical inspection was performed.

The implementation status should therefore not be interpreted as proof of operational effectiveness.

## 5. Conclusion

The assessment identified significant weaknesses in access control, data protection, business continuity, and security monitoring.

Although several basic technical and physical controls are implemented, the organization requires improvements to reduce its exposure to security incidents.

The findings documented here will serve as input for the subsequent risk assessment and remediation plan.
