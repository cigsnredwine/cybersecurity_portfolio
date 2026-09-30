# Botium Toys — Internal Security Audit Lab

Completed a document-based internal security audit exercise for Botium Toys, a fictional toy retailer expanding its online business internationally.

## Scope and my contribution

The lab supplied the IT manager's scope, goals, asset information, and risk assessment, along with a controls and compliance checklist. I reviewed the supplied evidence, completed the checklist, and wrote recommendations for improving the company's security posture.

The assessment covered 14 security controls and 12 checklist items grouped under PCI DSS, GDPR, and SOC Type 1/Type 2. These are the worksheet's training categories. The scenario introduces NIST CSF as the basis for the audit.

**Skills practiced:** Security control assessment, risk assessment review, compliance gap identification, and written security recommendations.

## Evidence

- [Completed controls and compliance checklist — my lab submission](./documents/completed-controls-compliance-checklist.pdf)
- [Provided scope, goals, and risk assessment — lab reference material](./documents/provided-scope-goals-risk-assessment.pdf)

The reference report's risk score of **8/10** was supplied by the exercise; I did not calculate it.

## Findings

| Area | Evidence in the supplied report | Assessment |
| --- | --- | --- |
| Access restrictions | All employees can access internally stored data; least privilege and separation of duties are absent. | Excessive access increases exposure of customer and payment information. |
| Encryption | Internally handled credit card data is not encrypted. | Sensitive payment data lacks an important protection. |
| Recovery | Critical-data backups and disaster recovery plans are absent. | Recovery from data loss or disruption is not adequately planned. |
| Detection | A firewall and antivirus are present, but an intrusion detection system is absent. | The scenario identifies a gap in intrusion detection coverage. |
| Password practices | A password policy exists but its requirements are minimal; centralized password management is absent. | Password controls need strengthening. |
| Legacy systems | Maintenance occurs without a regular schedule or clear intervention methods. | The maintenance process needs formal procedures. |
| Physical protection | Locks, CCTV, and fire detection/prevention are present. | Existing physical safeguards are documented. |

My completed control checklist marked **5 controls present and 9 absent or inadequate**. These answers reflect the scenario documents rather than technical tests.

## Recommendations documented in my checklist

- Apply least privilege and separation of duties to restrict sensitive-data access.
- Establish a disaster recovery plan.
- Strengthen password requirements and introduce centralized password management.
- Add intrusion detection capabilities.
- Formalize ongoing maintenance and intervention procedures for legacy systems.
- Encrypt sensitive information.
- Clarify and classify assets to identify appropriate additional protections.
