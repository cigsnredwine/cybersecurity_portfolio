# Security Risks of Third-Party APIs & Developer Behavior

## Overview
This research project examines cybersecurity risks introduced by third-party APIs, software supply chains, credential leakage, and AI-assisted development.

The paper analyzes the 2026 Vercel security breach as a case study of a third-party OAuth compromise, as well as the Axios npm supply chain compromise. It also explores exposed secrets in GitHub repositories, risks in AI-generated code, and mitigation strategies such as least privilege, zero trust architecture, dependency auditing, and credential scanning.

## Topics Covered
- Third-party API security
- OAuth and identity compromise
- Software supply chain security
- npm dependency risks
- Secret and credential leakage
- AI-assisted development risks
- Principle of least privilege
- Zero trust architecture

## Case Studies

### Vercel OAuth Breach
Analyzed how a compromised third-party OAuth application created an attack path into Vercel's environment through stolen OAuth tokens and trusted identity relationships.

### Axios npm Supply Chain Compromise
Examined how malicious package versions and dependency installation behavior can introduce security risks into software projects.

## Key Findings
- Third-party integrations can create indirect attack paths into trusted systems.
- OAuth tokens can act as delegated credentials and bypass password-based authentication.
- Software dependency ecosystems can spread vulnerabilities across many applications.
- Exposed secrets may remain active long after they are published.
- AI-generated code should be reviewed using the same security standards as externally sourced code.

## Mitigation Strategies
The paper discusses:
- Principle of least privilege
- Limiting OAuth scopes
- Regular access audits
- Zero trust architecture
- Static analysis
- Dependency auditing
- Credential scanning
- Manual review of AI-generated code

## Full Research Paper
[View the full paper](./CISC3600-Final-Project.pdf)
