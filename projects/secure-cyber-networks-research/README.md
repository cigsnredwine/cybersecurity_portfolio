# Security Risks of Third-Party APIs & Developer Behavior

## Overview

For a Secure Cyber Networks course, I wrote a research paper examining risks from third-party APIs, software supply chains, exposed credentials, and AI-assisted development. Using Vercel OAuth and Axios npm case studies, I connected these risks to mitigation approaches including least privilege, dependency auditing, credential scanning, and secure code review.

## Tools and Topics

- **API and OAuth security:** Third-party access and delegated credentials.
- **Software supply chains:** npm dependencies and package compromise.
- **Secret management:** Exposed credentials and credential scanning.
- **Secure development:** AI-generated code review, least privilege, and zero trust.

## Workflow

1. **Defined the research scope.** Examined how third-party APIs, dependencies, developer practices, and AI-assisted coding can introduce security risks.
2. **Analyzed the case studies.** Used the Vercel incident bulletin and published security analyses to describe the OAuth attack chain. Compared that with Microsoft’s Axios analysis and research on how vulnerabilities propagate through npm dependencies.
3. **Examined credential exposure.** Reviewed GitGuardian’s State of Secrets Sprawl 2026 report, discussing hardcoded credentials, delayed rotation, and the difference between exposure in public and internal repositories.
4. **Reviewed AI-assisted development risks.** Analyzed a published study of 7,703 AI-attributed files assessed with CodeQL and CWE classifications, then discussed its findings on language-specific weaknesses. This was a review of the study, not a CodeQL scan I performed.
5. **Connected risks to mitigations.** Covered least privilege, restricted OAuth scopes, access reviews, zero trust, dependency auditing, credential scanning, static analysis, and manual code review.
6. **Compiled the research paper.** Organized the case studies, figures, findings, and mitigation discussion into a final submission with nine references, including NIST SP 800-53 and SP 800-207.

## Results

Produced a research paper connecting integration and development risks to practical security controls. The work demonstrates security research and written analysis; it does not include hands-on exploitation or validation of the incidents discussed.

## Materials

- [My research paper](./CISC3600%20Final%20Project%20-%20Jayden%20Nguyen.pdf)
