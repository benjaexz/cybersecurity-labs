
# Risk Assessment

## 1. Assessment Scope

This document evaluates the information security risks identified during the educational assessment of the fictional organization Botium Toys.

The assessment is based on the findings documented in `controls-assessment.md`, `compliance-gap-analysis.md`, and `security-findings.md`.

The objective is to estimate risk levels, identify business consequences, and establish remediation priorities.

This is a qualitative risk assessment based on the available case study evidence. No technical testing, independent validation, or quantitative loss analysis was performed.

## 2. Risk Assessment Methodology

Risk is evaluated using two dimensions:

- **Likelihood:** The relative likelihood of a threat scenario occurring, considering the available evidence and identified control deficiencies.
- **Impact:** The potential consequences to confidentiality, integrity, availability, operations, finances, and reputation.

The risk score is calculated as:

Risk Score = Likelihood × Impact

This is a project-defined qualitative scoring model. The resulting scores are prioritization indicators, not statistically measured probabilities or expected financial losses.

Both dimensions use a scale from 1 to 5.

### 2.1 Likelihood Scale

| Score | Rating | Description |
|---:|---|---|
| 1 | Rare | The scenario is highly unlikely under current conditions. |
| 2 | Unlikely | The scenario could occur, but is not expected frequently. |
| 3 | Possible | The scenario is plausible and may occur. |
| 4 | Likely | The scenario has a substantial probability of occurring. |
| 5 | Almost Certain | The scenario is expected to occur frequently or under current conditions. |

### 2.2 Impact Scale

| Score | Rating | Description |
|---:|---|---|
| 1 | Negligible | Minimal operational or business consequences. |
| 2 | Minor | Limited disruption or recoverable losses. |
| 3 | Moderate | Noticeable operational disruption or financial impact. |
| 4 | Major | Significant business disruption, sensitive data exposure, or substantial financial consequences. |
| 5 | Severe | Critical business disruption, extensive sensitive data exposure, or potentially catastrophic consequences. |

### 2.3 Risk Classification

The risk score determines the qualitative classification:

| Risk Score | Classification |
|---:|---|
| 1–4 | Low |
| 5–9 | Moderate |
| 10–16 | High |
| 17–25 | Critical |

### 2.4 Inherent and Residual Risk

**Inherent Risk**

The level of risk before considering the effect of existing security controls.

**Residual Risk**

The level of risk remaining after considering existing controls and their estimated effectiveness.

Because the effectiveness of existing controls was not independently validated, residual risk ratings in this assessment are preliminary estimates.

## 3. Assessment Limitations

The assigned likelihood and impact scores represent analytical judgments based on the information available in the educational case study.

They should not be interpreted as statistically measured probabilities or confirmed incident frequencies.

Risk scores may change after technical validation, additional evidence collection, and assessment of control effectiveness.


## 4. Risk Register

The following risk register translates the identified security findings into risk scenarios.

Scores are preliminary analytical estimates based on the case study evidence.

| ID | Risk Scenario | Likelihood | Impact | Inherent Risk | Existing Controls | Residual Risk | Priority |
|---|---|---:|---:|---|---|---|---|
| R-01 | Unauthorized access to sensitive information due to excessive privileges. | 4 | 5 | 20 - Critical | No effective least-privilege implementation identified. | 20 - Critical | Immediate |
| R-02 | Exposure of payment card information due to insufficient cryptographic protection. | 4 | 5 | 20 - Critical | Firewall and antivirus are present, but they do not replace data encryption. | 20 - Critical | Immediate |
| R-03 | Permanent data loss or prolonged service disruption due to missing backups and disaster recovery procedures. | 4 | 4 | 16 - High | No backup or disaster recovery capabilities identified. | 16 - High | High |
| R-04 | Delayed detection of malicious activity due to the absence of dedicated intrusion detection. | 4 | 4 | 16 - High | Firewall, antivirus, and manual monitoring are present; their effectiveness in detecting intrusions has not been validated. | 16 - High | High |
| R-05 | Account compromise and unauthorized operations due to weak authentication and access governance. | 4 | 4 | 16 - High | Password policy exists but has weak requirements. No centralized password management or separation of duties. | 16 - High | High |

## 5. Risk Analysis and Justification

### R-01 — Excessive Access Privileges

**Inherent Risk: 20 — Critical**

**Residual Risk: 20 — Critical**

Broad employee access to sensitive information increases the potential for unauthorized disclosure following credential compromise or insider misuse.

The absence of effective least-privilege controls provides little evidence of risk reduction.

**Risk Treatment:** Implement role-based access control, restrict permissions according to job responsibilities, and conduct periodic access reviews.

### R-02 — Unencrypted Payment Card Data

**Inherent Risk: 20 — Critical**

**Residual Risk: 20 — Critical**

Payment card information without appropriate cryptographic protection may be exposed if an attacker gains access to systems, storage, or network communications handling this information.

The existing firewall and antivirus controls do not directly address the lack of encryption.

**Risk Treatment:** Implement appropriate cryptographic protections, secure key management, tokenization where applicable, and data minimization.

### R-03 — Missing Backup and Disaster Recovery Capabilities

**Inherent Risk: 16 — High**

**Residual Risk: 16 — High**

The absence of backups and disaster recovery procedures creates a substantial risk of permanent data loss and prolonged operational disruption.

No effective recovery controls were identified in the available evidence.

**Risk Treatment:** Establish a backup strategy, maintain isolated or immutable copies, define RTO and RPO, and regularly test restoration procedures.

### R-04 — Missing Intrusion Detection Capability

**Inherent Risk: 16 — High**

**Residual Risk: 16 — High**

The absence of dedicated intrusion detection reduces visibility into suspicious network and system activity.

Although firewall, antivirus, and manual monitoring controls are present, the available evidence does not establish their effectiveness in detecting malicious activity.

**Risk Treatment:** Deploy appropriate IDS or EDR capabilities, centralize security logs, and establish alert investigation procedures.

### R-05 — Weak Authentication and Access Governance

**Inherent Risk: 16 — High**

**Residual Risk: 16 — High**

Weak password requirements and the absence of centralized password policy enforcement increase the likelihood of account compromise.

The lack of separation of duties also increases the risk of unauthorized or conflicting operations.

**Risk Treatment:** Implement centralized identity and access management, enforce MFA, strengthen authentication policies, and establish separation of duties.

## 6. Risk Treatment Priorities

Based on the preliminary risk ratings, the recommended remediation order is:

| Priority | Risk IDs | Recommended Focus |
|---|---|---|
| Immediate | R-01, R-02 | Restrict excessive access and protect payment card information. |
| High | R-03, R-04, R-05 | Establish recovery capabilities, improve detection, and strengthen identity controls. |

Risk treatment should consider technical feasibility, business requirements, implementation costs, and applicable regulatory obligations.

## 7. Residual Risk Considerations

Residual risk represents the estimated exposure remaining after considering existing controls.

In this assessment, R-04 retains its inherent score because the available evidence does not establish that existing monitoring and protective controls meaningfully reduce the risk of delayed intrusion detection.

The other risks retain their inherent scores because the available evidence does not demonstrate effective controls that meaningfully reduce their exposure.

These estimates must be reassessed after remediation and independent validation of control effectiveness.

## 8. Conclusion

The assessment identifies two Critical risks involving excessive access privileges and unprotected payment card information.

Three additional High risks affect business continuity, threat detection, and identity and access governance.

The organization should prioritize reducing exposure of sensitive information while strengthening its ability to detect incidents and recover from operational disruptions.

A formal risk management process should periodically review these ratings as new evidence becomes available.
