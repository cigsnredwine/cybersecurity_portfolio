# CompTIA Security+ SY0-801 V8 Study Guide

> **AI-assisted study resource:** Developed with Codex from a supplied exam-objectives document. Structure and internal links were checked with automated tools; this is not a claim of exhaustive subject-matter review or an official CompTIA publication. See [process and attribution](README.md).

Based on the uploaded **CompTIA Security+ SY0-801 Exam Objectives, Version 2.0**. This guide preserves objectives 1.1–5.6 and explains each listed concept in original study notes. Examples are illustrative, not exam questions. The objectives say their examples are not exhaustive; learn how to apply the concepts as well as recognize the vocabulary.

## Clickable index

- [How to use this guide](#how-to-use-this-guide)
- [1.0 General Security Concepts — 16%](#10-general-security-concepts--16)
  - [1.1 Security concepts and controls](#11-explain-security-concepts-and-controls)
  - [1.2 Change management](#12-given-a-scenario-demonstrate-the-impact-of-change-management-processes-on-security)
  - [1.3 Cryptographic solutions](#13-explain-the-importance-of-using-appropriate-cryptographic-solutions)
- [2.0 Threats, Vulnerabilities, and Attacks — 24%](#20-threats-vulnerabilities-and-attacks--24)
  - [2.1 Threat and vulnerability characteristics](#21-explain-characteristics-of-threats-and-vulnerabilities)
  - [2.2 Threat actors and motivations](#22-describe-common-threat-actors-and-motivations)
  - [2.3 Threat vectors and sources](#23-describe-threat-vectors-and-sources)
  - [2.4 Vulnerabilities and attack surfaces](#24-explain-types-of-vulnerabilities-and-attack-surfaces)
  - [2.5 Indicators of malicious activity](#25-given-a-scenario-analyze-indicators-of-malicious-activity)
  - [2.6 Artificial intelligence risks](#26-summarize-threats-and-vulnerabilities-associated-with-artificial-intelligence-usage)
- [3.0 Security Architecture — 19%](#30-security-architecture--19)
  - [3.1 Architecture models](#31-compare-and-contrast-security-implications-of-different-architecture-models)
  - [3.2 Protecting infrastructure](#32-given-a-scenario-manage-the-security-architecture-to-best-protect-the-infrastructure)
  - [3.3 Protecting data](#33-summarize-concepts-and-strategies-used-to-protect-data)
  - [3.4 Resilience and recovery](#34-explain-the-importance-of-resilience-and-recovery-in-security-architecture)
- [4.0 Security Operations — 27%](#40-security-operations--27)
  - [4.1 Mitigating controls](#41-given-a-scenario-apply-mitigating-controls-techniques-and-solutions-to-secure-the-environment)
  - [4.2 Asset management](#42-explain-the-security-implications-of-proper-hardware-software-and-data-asset-management)
  - [4.3 Vulnerability management](#43-given-a-scenario-perform-tasks-associated-with-vulnerability-management)
  - [4.4 Alerting and monitoring](#44-explain-security-alerting-and-monitoring-concepts-and-tools)
  - [4.5 Identity and access management](#45-given-a-scenario-apply-concepts-related-to-identity-and-access-management)
  - [4.6 Automation and orchestration](#46-given-a-scenario-apply-automation-and-orchestration-solutions-to-secure-operations)
  - [4.7 Incident response](#47-summarize-concepts-associated-with-incident-response-activities)
  - [4.8 Investigation data and artifacts](#48-given-a-scenario-use-data-artifacts-and-sources-to-support-a-security-investigation)
- [5.0 Security Program Management and Oversight — 14%](#50-security-program-management-and-oversight--14)
  - [5.1 Governance, risk, and compliance artifacts](#51-explain-the-importance-of-governance-risk-and-compliance-artifacts)
  - [5.2 Risk management](#52-explain-the-impact-of-risk-management-processes-on-the-security-of-the-organization)
  - [5.3 Third-party risk](#53-explain-the-assessment-and-management-processes-associated-with-third-party-risk)
  - [5.4 Compliance](#54-summarize-elements-of-effective-security-compliance)
  - [5.5 Audits and assessments](#55-explain-concepts-associated-with-audit-and-assessment-activities)
  - [5.6 Security awareness](#56-given-a-scenario-apply-security-awareness-concepts-to-improve-organizational-security)
- [Glossary of important distinctions](#glossary-of-important-distinctions)
  - [Foundations and cryptography](#foundations-and-cryptography)
  - [Threats and vulnerabilities](#threats-and-vulnerabilities)
  - [Architecture and data](#architecture-and-data)
  - [Operations and identity](#operations-and-identity)
  - [Governance and risk](#governance-and-risk)
- [Complete acronym glossary](#complete-acronym-glossary)
  - [A–C](#ac)
  - [D–H](#dh)
  - [I–N](#in)
  - [O–R](#or)
  - [S–X](#sx)
  - [Additional acronyms used in this guide or objectives](#additional-acronyms-used-in-this-guide-or-objectives)
- [Scenario practice and self-checks](#scenario-practice-and-self-checks)
- [Sources and terminology notes](#sources-and-terminology-notes)

## How to use this guide

For each concept, be able to define it, identify evidence of it, choose an appropriate control, and explain a tradeoff. For scenario objectives, ask: **What asset is at risk? What is the immediate goal? What evidence supports the decision? What must be preserved?** Cover every domain; weights indicate emphasis, not permission to skip sections.

Tables group closely related concepts while keeping the Portable Document Format (PDF) source's order. Acronyms are expanded when first introduced in the instructional text and again in the acronym glossary. Classification names and organizational processes vary; use the scenario's stated policy. Technical examples are study illustrations, not universal configuration prescriptions.

## 1.0 General Security Concepts — 16%

### 1.1 Explain security concepts and controls

#### Defense in depth

**Defense in depth** uses multiple complementary safeguards so one failure does not expose everything. Example: an email filter, staff training, limited account permissions, endpoint monitoring, and tested backups each address a different part of a ransomware incident.

| Concept | Definition and practical example |
|---|---|
| Confidentiality, integrity, and availability (CIA) | Confidentiality prevents unauthorized disclosure; integrity prevents or detects unauthorized alteration; availability keeps services usable when needed. Encryption protects payroll secrecy, signatures help detect tampering, and redundant servers support access. |
| Authentication, authorization, and accounting (AAA) | Authentication establishes who or what is requesting access; authorization determines allowed actions; accounting records activity. A user signs in, can read only their department's files, and their downloads are logged. |
| Non-repudiation | Evidence that makes falsely denying an action difficult. A properly implemented digital signature links a signed transaction to a protected signing key. Shared accounts weaken attribution. |
| Zero Trust principles | Do not grant implicit trust merely because a device is on an internal network. Explicitly verify identity and device context, minimize permissions, and assume breaches are possible. Reassess access as conditions change. |
| Least privilege | Grant only the permissions necessary, for the needed duration. A backup service can read protected files without having unrestricted administrator access. |

#### Control categories

| Category | Meaning and example |
|---|---|
| Technical/logical | Technology-enforced safeguards: encryption, access rules, authentication. |
| Managerial/administrative | Governance and management decisions: risk assessments, policies, security planning. |
| Physical/environmental | Protection of facilities and operating conditions: locks, cooling, smoke detection. |
| Operational | Safeguards implemented through daily people/process activities: badge checks, backup procedures, incident handling. |

#### Control types

| Type | Purpose and example |
|---|---|
| Preventive | Stops an event: deny unauthorized connections with a firewall. |
| Deterring | Discourages an attempt: visible cameras or warning signs. The PDF says “deterring”; “deterrent” is common terminology. |
| Corrective | Repairs damage or restores a safe state: remove malware and restore files. |
| Detective | Reveals an event: an alert for an unexpected privileged login. |
| Compensating | Provides an alternative safeguard when the preferred control is impractical: isolate a legacy system that cannot be patched. It must address the relevant risk. |
| Directive | Tells people what to do: a policy requiring visitors to be escorted. |

**Exam distinction:** Category describes how a control is implemented; type describes its purpose. A camera is physical and usually detective, and its visibility can also deter.

### 1.2 Given a scenario, demonstrate the impact of change management processes on security

#### Business processes impacting security operations

| Concept | Definition and practical example |
|---|---|
| Change advisory board (CAB); approval process | A review body assesses proposed changes and approvals according to policy. A firewall change is reviewed for exposure, business impact, testing, and recovery steps before implementation. |
| Ownership | A named person is accountable for the change and its results. A service owner approves business downtime; an implementer executes the work. |
| Stakeholders | People affected or needed for success: users, operations, security, vendors, and business owners. Notify teams that depend on the altered service. |
| Impact analysis | Predict effects on security, availability, dependencies, users, and compliance. Closing a port may stop an attack path but also break a payment integration. |
| Test results | Evidence that the change works and avoids unacceptable side effects. Test expected traffic and blocked traffic, not just whether a service starts. |
| Backout planning | Document how to return to the previous safe state, including triggers and deadlines. Save the old configuration and verify that rollback remains feasible. |
| Fail forward | Recover by completing or correcting the new state rather than reverting. A database migration may require a follow-up fix because rollback would lose new transactions. |
| Maintenance window | A scheduled period for changes with approved disruption. Confirm staffing and dependency availability during the window. |
| Standard operating procedures (SOPs) | Repeatable, approved instructions for routine work. A certificate renewal procedure includes testing, deployment, and monitoring. |

#### Technical implications

| Concept | Definition and practical example |
|---|---|
| Allow lists/deny lists | Permit explicitly approved items or reject explicitly prohibited ones. Updating an allow list may be necessary when a legitimate application's signing certificate changes. |
| Restricted activities | Actions limited during a change, such as a deployment freeze or prohibiting simultaneous database edits. |
| Downtime | Period when a service is unavailable. Include expected downtime and an overrun decision point in the plan. |
| Service restart | Restart a background component to load configuration; dependent services may briefly lose connectivity. |
| Application restart | Restart an application to activate an update; users may lose sessions or unsaved work. |
| Legacy applications | Older applications may rely on outdated protocols, libraries, or unsupported platforms. Test compatibility before enforcing new controls. |
| Dependencies | Components that must operate together. A login service may depend on a directory, name resolution, certificates, and accurate clocks. |

#### Documentation and version control

- **Updating diagrams:** Reflect new network paths, security zones, devices, and trust boundaries. An obsolete diagram can cause an incident responder to isolate the wrong system.
- **Updating policies/procedures:** Record changed responsibilities, requirements, and operating steps. Documentation must match the implemented configuration.
- **Version control:** Retain change history, approved revisions, and identifiable versions. It enables comparison, accountability, and restoration; protect the repository and keep secrets out of it.

**Scenario:** Before disabling an obsolete encryption protocol, identify clients that use it, test replacements, obtain approval, schedule the change, define rollback or fail-forward criteria, update documentation, and monitor results.

### 1.3 Explain the importance of using appropriate cryptographic solutions

#### Public key infrastructure

**Public key infrastructure (PKI)** combines certificates, authorities, keys, policies, and processes to establish trust in public keys.

| Concept | Definition and example |
|---|---|
| Public key | A shareable key used to verify signatures or, in suitable schemes, encrypt data to its owner. Sharing it does not expose the paired private key. |
| Private key | A secret key used to sign or decrypt, depending on the scheme. Theft can permit impersonation; storage and access protection are essential. |
| Key escrow | An authorized recovery arrangement that holds keys or recovery material with a trusted party. It supports recovery but creates a sensitive target and requires controlled access. |

#### Certificates

| Concept | Definition and example |
|---|---|
| Certificate authorities | Trusted entities that bind identities to public keys through signed certificates. Validate the chain and intended usage, not merely the presence of a certificate. |
| Certificate revocation lists (CRLs) | Published lists of certificates revoked before expiration. A cached list can be stale. |
| Online Certificate Status Protocol (OCSP) | A protocol for obtaining a certificate's revocation status. Availability, freshness, and client handling affect protection. |
| Self-signed | Signed by its own private key. Useful in controlled environments when trust is explicitly provisioned; not automatically trusted by external clients. |
| Third-party | Issued by an external authority trusted by the relying party. Identity validation and chain validation still matter. |
| Root of trust | The trusted starting point for verification, such as a root certificate or hardware trust anchor. A root certificate in a trust store anchors a certificate chain. |
| Certificate signing request (CSR) generation | Produce a request containing a public key and identity details, signed using the corresponding private key. Keep the private key secret; do not send it to the issuer. |
| Wildcard | A certificate covering names under a specified domain pattern. `*.example.com` normally covers `shop.example.com`, not the base domain or multiple nested levels unless separately included. Broad coverage increases the impact of key theft. |

#### Encryption

**Encryption** transforms readable plaintext into ciphertext using an algorithm and key. It protects confidentiality; integrity needs an authenticated construction or separate integrity protection.

| Concept | Definition and practical example |
|---|---|
| Protocols | Rules governing secure exchanges, including negotiation and verification. Transport Layer Security (TLS) protects many client-server communications; Internet Protocol Security (IPSec) can protect network traffic. |
| Symmetric | The same secret key encrypts and decrypts. Efficient for bulk data, but safe distribution of the key is a challenge. |
| Asymmetric | Uses a mathematically related public/private key pair. Supports signatures and key establishment; usually paired with symmetric encryption for bulk data. |
| Full disk | Encrypts the disk's protected contents at rest. Helps against stolen powered-off devices; an unlocked machine may still expose data. |
| Partition | Encrypts a selected disk partition. Other partitions may remain readable. |
| File | Encrypts individual files; filenames or metadata may remain visible depending on the system. |
| Volume | Encrypts a logical storage volume, which may span storage devices. |
| Database | Encrypts a database or database storage. Authorized queries may still return plaintext. |
| Record | Encrypts selected records or fields. Useful for especially sensitive values with narrower key access. |
| Transport/communication | Encrypts data while moving between endpoints. Hop-by-hop protection can expose data at intermediaries; end-to-end protection confines decryption to intended endpoints. |
| Key exchange | Establishes shared keying material securely. Authenticate the parties to prevent an attacker substituting their own exchange. |
| Algorithms | Mathematical methods implementing encryption, hashing, or signatures. Select well-reviewed algorithms and appropriate modes; custom cryptography is difficult to secure. |
| Key length | Size of the key and one contributor to security. Different algorithm families cannot be compared by bit length alone. Long keys do not fix poor randomness or stolen keys. |

#### Other cryptographic concepts

- **Digital signatures:** A private key signs data and a public key verifies it, supporting integrity, origin authentication, and evidence for non-repudiation. Signing does not hide the message.
- **Salting:** Add a unique random value to each password before applying a password-hashing scheme. It prevents identical passwords from having identical stored hashes and limits reuse of precomputed attacks. Salts are usually stored with hashes; they are not encryption keys.
- **Tools:** Certificate utilities, key-management services, hardware-protected key stores, disk encryption tools, and cryptographic libraries perform different jobs. Prefer protected key generation/storage and established libraries; verify a tool's defaults and permissions.
- **Obfuscation:** Makes information harder to understand without necessarily providing cryptographic confidentiality. Encoding or scrambled variable names are not substitutes for encryption.
- **Hashing algorithms:** Produce a digest useful for integrity checks and identifiers. A hash cannot generally be “decrypted.” Password storage needs a dedicated, deliberately expensive password-hashing scheme, not a fast general-purpose hash alone.

**Exam distinction:** Encryption hides content; hashing summarizes content; signatures authenticate signed content. A hash from an untrusted source does not prove a file is trustworthy.

## 2.0 Threats, Vulnerabilities, and Attacks — 24%

### 2.1 Explain characteristics of threats and vulnerabilities

A **threat** is a potential cause of harm; a **vulnerability** is a weakness that could be exploited. **Risk** depends on the possibility of harm and its consequences. An **exploit** is a method of taking advantage of a weakness.

#### Threats

| Concept | Definition and example |
|---|---|
| Threat feeds | Streams of indicators or intelligence, such as malicious domains. Evaluate freshness, relevance, provenance, and false positives before blocking. |
| Likelihood | How probable an event is in a given context. An internet-facing vulnerable service is generally more exposed than an isolated equivalent. |
| Impact | Expected harm: service interruption, disclosure, financial loss, or physical consequences. A brief outage can be severe for a safety-critical service. |
| Intelligence sources | Internal logs, vendor advisories, government alerts, research, and information-sharing groups. Corroborate sources and distinguish raw data from analyzed intelligence. |
| Life cycle | Threat activity develops from preparation and reconnaissance through access, persistence, actions, and possible cleanup. Intelligence also has a collection-analysis-distribution-feedback cycle; the PDF does not specify one model here. |

#### Vulnerabilities

| Concept | Definition and example |
|---|---|
| Scoring; Common Vulnerability Scoring System (CVSS) | A structured way to describe vulnerability severity. A severity score does not alone establish your organization's risk or prove exploitation. |
| Prioritization | Order remediation using severity, exploitation evidence, exposure, asset importance, and available controls. An actively exploited medium-severity flaw can outrank an inaccessible high-severity flaw. |
| Vulnerability types | Software defects, configuration errors, weak credentials, design weaknesses, and process/control gaps. Some are fixed by patches; others need configuration or workflow changes. |
| Common Vulnerabilities and Exposures (CVE) | Identifiers for publicly disclosed vulnerabilities. One identifier names a specific vulnerability; it is not its score or the patch itself. |

### 2.2 Describe common threat actors and motivations

#### Threat actors

| Actor | Typical characteristics and example |
|---|---|
| Crime syndicate/organized crime | Coordinated profit-seeking groups; credential theft, fraud, and extortion operations. |
| Terrorist | Seeks fear or disruption to advance an ideology; may target critical infrastructure. |
| Unskilled attacker | Uses readily available tools with limited expertise; can still cause serious harm. |
| Hacktivist | Uses attacks to advance a social or political cause; defacement or service disruption. |
| Insider | Has or had legitimate access; may steal data or deliberately sabotage systems. Contractors can be insiders too. |
| Accidental/unintentional | Causes harm without malicious intent, such as sharing a confidential folder publicly. |
| Competitor | Seeks business advantage, such as access to proprietary designs. |
| State-sponsored | Supported by a government; may pursue strategic espionage or disruption with substantial resources. |

#### Motivations

| Motivation | Meaning/example |
|---|---|
| Financial | Steal funds, monetize accounts, or sell data. |
| Influence | Shape beliefs, decisions, or public perception. |
| Intellectual property | Obtain designs, research, algorithms, or trade secrets. |
| Notoriety | Gain recognition or status. |
| Espionage | Secretly collect strategic or sensitive intelligence. |
| Fear/chaos | Create alarm, confusion, or instability. |
| Extortion | Demand payment by threatening disruption or disclosure. |
| General curiosity | Explore systems, sometimes without understanding boundaries or harm. |
| Revenge | Retaliate for a perceived wrong. |
| Ideological | Advance a belief system or cause. |
| Political | Affect government, elections, or policy. |
| Ethical | Authorized research to identify and responsibly disclose weaknesses. Benevolent intent alone does not authorize access. |

#### Attributes of actors

**Internal/external** describes access and relationship to the organization. **Resources/funding** affects scale and persistence. **Sophistication/capability** describes technical and operational ability. Do not identify an actor solely from a tool: a simple attack can be used by a sophisticated group, and multiple motivations can coexist.

### 2.3 Describe threat vectors and sources

A **vector** is the route used to reach a target. An **advanced persistent threat (APT)** is a capable, sustained campaign or actor pursuing long-term objectives; it is not a single malware type.

| Vector/source and listed components | Definition and practical example |
|---|---|
| Message-based: email; Short Message Service (SMS); Rich Communication Services (RCS); instant messaging; collaboration tools | Messages deliver malicious links, files, impersonation, or urgent requests. A compromised colleague's collaboration account can make an attack appear internal and trustworthy. |
| Image-based: Quick Response (QR) codes; embedded content; Completely Automated Public Turing test to tell Computers and Humans Apart (CAPTCHA) | Images can conceal destinations or carry embedded data. A fake CAPTCHA page may instruct a user to run a harmful command. The test itself is not inherently malicious; attackers abuse the surrounding workflow. |
| Attachment-based: embedded macros; Rich Text Format (RTF); Portable Document Format (PDF) | Files may contain active code, exploit a reader, or link to credential theft pages. A document asking the user to enable macros is a warning sign. The source uses “Portable Document Formats”; the standard expansion is singular. |
| Browser-based: extensions; JavaScript; password managers; cookies; session tokens | Malicious scripts or extensions can steal information and authenticated sessions. A password manager is normally protective, but a malicious extension, compromised vault, or fake manager can become an entry point. |
| Network-based: infrastructure devices; virtualized devices; session keys | Routers, firewalls, virtual appliances, and keying material may be compromised. A stolen session key may expose protected traffic; a weakly managed virtual firewall can permit lateral movement. |
| Remote access: remote desktop; Virtual Network Computing (VNC); virtual private network (VPN) | Remote administration and connectivity expand access paths. Exposed services, weak credentials, or an unpatched gateway can provide entry. |
| Endpoint-based: mobile devices; workstations; servers; tablets; trusted devices | Compromise a device to access accounts or data. “Trusted” describes an assigned status, not proof a device is clean. |
| Built-in tools; living-off-the-land tools | Attackers reuse legitimate utilities to execute actions or maintain access. A normal shell or administrative utility running under an unexpected account can be suspicious even without a new malware file. |
| Supply chain-based: third-party providers; managed service providers; logistic providers; Software as a Service (SaaS) providers | Compromise a trusted dependency or partner. A vendor's remote-management account or a tampered delivered device can affect many customers. |
| External media-based: malicious Universal Serial Bus (USB) | Removable devices can carry malware, emulate keyboards, or attack device firmware. A found USB drive is not safe simply because a malware scan is clean. |
| Human-based: impersonation; contractor; visitor; biometric; watering hole | Abuse trust or identity workflows. A fake contractor requests access; a spoofed biometric may defeat poorly designed verification. A watering hole compromises a site likely to be visited by a target group. |
| Internet of Things (IoT): cameras; sensors; printers | Connected appliances may have weak updates, passwords, or segmentation. A compromised printer can expose documents and provide a network foothold. |
| Operational technology (OT) | Systems that monitor or control physical processes. Compromise can change equipment behavior and create safety consequences. |
| Physical-based: lock and key; access vestibule; access passes | Lost keys, copied passes, bypassed locks, or misuse of controlled entry spaces enable unauthorized physical access. An access vestibule controls passage through sequential doors. |
| Signal-based: Bluetooth; radio frequency (RF); near-field communication (NFC) | Wireless proximity or radio interfaces can expose pairing, authentication, or data-exchange weaknesses. A relay attack can extend an apparent proximity interaction. |

### 2.4 Explain types of vulnerabilities and attack surfaces

An **attack surface** is the set of exposed interfaces, identities, processes, and assets that could be attacked.

| Concept | Definition and practical example |
|---|---|
| Unsupported products | Vendor support/security fixes have ended. Replace, isolate, or otherwise control them. |
| Unpatched systems | Available fixes have not been applied. Confirm dependencies and prioritize exposure, then verify remediation. |
| Obsolete systems | Technology no longer suitable for current needs, even if some support remains. It may lack needed security features. |
| Unmanaged systems | Assets outside inventory, configuration, or monitoring processes. An unknown server can miss every patch cycle. |
| Ports and services | Listening interfaces expose functionality. Disable unnecessary services and restrict required ones. |
| Applications: race conditions | Outcomes depend on timing or concurrent actions. An attacker changes a resource between validation and use. |
| Time-of-check (TOC); time-of-use (TOU) | A check succeeds, but the checked object changes before it is used. Checking a file's permissions and later opening a replaced file illustrates the gap. Use atomic operations where appropriate. |
| Malicious update | A tampered or compromised update installs harmful code. Validate provenance, signatures, and deployment behavior. |
| Code: hardcoded secrets | Passwords or keys embedded in code, images, or configuration distributed with software. Moving code to a private repository does not remove exposed secrets; rotate them. |
| Unsafe exception handling | Errors reveal sensitive details, skip checks, or leave inconsistent state. A crash message should not disclose a database password. |
| Operating system (OS)-based | Kernel, driver, permission, or default-service weaknesses. A local flaw can elevate a limited user to administrator. |
| Virtualization | Hypervisor, management-plane, image, or isolation weaknesses. An escape from a guest can affect the host or other guests. |
| Zero-day | A vulnerability exploited or exposed before defenders have an effective available fix, commonly before vendor awareness or patch release. Apply layered controls and monitor while awaiting remediation. |
| Cryptographic vulnerabilities | Weak algorithms, poor randomness, bad certificate validation, reused nonces, or key exposure. Strong encryption fails if the private key is public. |
| Unmanaged/stale credentials | Secrets without ownership or obsolete accounts still usable. Disable former contractor access and rotate forgotten service credentials. |
| Rogue devices | Unauthorized or malicious devices, such as an unapproved wireless access point. |
| Shadow information technology (shadow IT) | Technology used without organizational approval/visibility. A department's private file-sharing account bypasses retention and access controls. |
| Wireless and low-powered communications | Radio exposure, insecure pairing, limited processing, and weak update capability can constrain safeguards. |
| Large language models (LLMs) | Models generating language can mishandle untrusted instructions, disclose data, or produce unreliable output; see 2.6. |
| Identity providers | Central identity services are high-impact targets. Bad federation configuration or stolen signing keys can enable broad impersonation. |
| Mobile devices | Loss, malicious applications, weak screen locks, outdated software, and insecure connections expose data. |
| Misconfiguration | Settings unintentionally weaken security. An administrative interface open to the internet is an example. |
| Public repositories | Accidental disclosure of secrets, internal code, or sensitive configuration. Scan history as well as current files. |
| Public object storage | Cloud objects exposed through public permissions or links. Public access should be deliberate, scoped, and monitored. |

### 2.5 Given a scenario, analyze indicators of malicious activity

#### Malware attacks

| Type | Meaning and likely evidence |
|---|---|
| Ransomware | Encrypts, disrupts, or steals data to demand payment. Mass file changes, ransom notes, and backup deletion are clues. |
| Trojan | Appears legitimate but performs hidden malicious actions. A fake installer also starts an unauthorized remote-access process. |
| Worm | Propagates between systems without needing a user to attach it to each new host. Repeated scanning and similar infections can indicate spread. |
| Spyware | Secretly collects information. Unexplained outbound reporting or surveillance behavior may be clues. |
| Adware | Delivers advertising, sometimes with intrusive tracking or unwanted installation. Unexpected redirects and browser changes are clues. |
| Virus | Infects a host file or program and spreads as infected content executes or moves. |
| Rootkit | Hides malicious activity or preserves privileged access by altering low-level behavior. System views may disagree with independent evidence. |
| Keylogger | Records keystrokes, through software or hardware, to obtain credentials or other data. |
| Logic bomb | Executes when a condition is met, such as a date or an account's deletion. |
| Fileless malware | Uses memory, scripts, registry data, or legitimate tools rather than relying primarily on a conventional executable file. It can still leave logs and persistence artifacts. |

#### Physical attacks

**Tailgating:** Follow an authorized person through a controlled door. **Shoulder surfing:** Observe screens or typed secrets. **Skimming:** Capture payment-card information through a concealed reader. **Forced entry:** Defeat or damage a physical barrier. Match badge records, footage, physical damage, and eyewitness accounts; one source rarely tells the whole story.

#### Network attacks

| Attack | Definition and example |
|---|---|
| Distributed denial of service (DDoS) | Many sources exhaust a service or link. A denial of service (DoS) need not be distributed. Rate limiting and upstream filtering address different bottlenecks. |
| Protocol downgrade | Force use of weaker security settings or protocols. Failed strong negotiation followed by an unexpected weak connection warrants investigation. |
| Rogue | An unauthorized network device/service, often impersonating a legitimate one. An unfamiliar access point copying the corporate network name is a clue. |
| Sniffing | Capture traffic for inspection or theft. Encryption limits readable contents but may not hide metadata. |
| Spoofing | Falsify identity or addressing information. An unexpected address-to-device mapping may indicate impersonation. |
| On-path | Position between communicating parties to observe, redirect, or modify exchanges. Correct certificate validation and authenticated encryption help resist it. |
| Domain Name System (DNS) attacks | Attack name resolution through tampering, hijacking, tunneling, or disruption. Unexpected answers or high-volume unusual queries can be clues. |
| Cache poisoning | Insert false information into a cache. A poisoned DNS cache redirects a legitimate hostname to an attacker-controlled destination. |

#### Social engineering attacks

| Attack | Definition and example |
|---|---|
| Smishing | Phishing through text messages: a fake delivery fee link. |
| Vishing | Voice-based deception: a fake help-desk caller requests a code. |
| Phishing | Deceptive messages seek access, money, or information. |
| Whaling | Targets senior or high-value personnel. |
| Spear phishing | Tailored phishing aimed at a specific person or group. |
| Quishing | Phishing through QR codes, such as a replaced parking-payment sticker. |
| Impersonation | Pretend to be a trusted identity or organization. Verify through an independently known channel. |
| Deepfake | Synthetic or altered media imitates a person. A convincing executive voice is not sufficient authorization for a payment. |

#### Indicators of compromise

| Indicator | Interpretation and limitation |
|---|---|
| Hash | Identifies a known file or artifact; changing the file changes its hash. A match requires reliable context. |
| Internet Protocol (IP) address; domain | May identify attack infrastructure. Shared hosting and reassignment can create false positives. |
| Malicious processes | Unexpected executable, parent-child chain, privileges, or network behavior. A familiar process name alone does not prove legitimacy. |
| File system artifacts | New persistence files, renamed documents, suspicious scripts, or unexpected scheduled-task definitions. |
| Timestamp | Helps build a timeline; clocks, time zones, and deliberate tampering can mislead. |
| Log manipulation | Missing entries, disabled logging, altered records, or unexplained gaps can indicate concealment. |
| Excessive resource consumption | Unusual processor, memory, disk, or network use may indicate mining, malware, or service exhaustion; legitimate workloads can do this too. |
| Plaintext strings | Readable commands, domains, paths, or messages in a file/memory image may reveal behavior. Treat them as clues, not proof of execution. |
| Account lockout | Repeated failed authentication may indicate attacks, stale credentials, or user error. |
| Impossible travel | Logins from implausibly distant locations in too little time. VPN exit locations can explain some cases. |
| Concurrent sessions | Simultaneous activity can indicate stolen credentials/tokens, but multiple devices may be legitimate. |

#### Application attacks

| Attack | Definition and example |
|---|---|
| Injection | Untrusted input becomes executable commands or queries. Structured Query Language (SQL) injection alters database queries; parameterized queries keep data separate from query structure. |
| Buffer overflow | Data exceeds a memory buffer, potentially causing a crash or code execution. Memory-safe design and bounds checking address the cause. |
| Replay | Reuse a previously valid message/token to perform an unauthorized action. Fresh challenges, expiration, and replay detection reduce risk. |
| Privilege escalation | Gain permissions beyond those authorized, vertically to a stronger role or horizontally to another user's resources. |
| Forgery | Fake a trusted request or artifact. A forged cross-site request may exploit a browser's authenticated session if the application lacks request protections. |
| Directory traversal | Manipulate paths to escape an intended directory, for example accessing protected files through parent-directory references. |

#### Credential attacks

**Password spraying:** Try a small number of common passwords across many accounts. **Brute force:** Systematically try many candidate passwords, often against one account or offline hash. **User enumeration:** Learn which usernames exist from responses or timing. **Replay:** Reuse captured authentication material. **Multifactor authentication (MFA) bypass:** Defeat additional verification through stolen sessions, adversary-controlled login proxies, weak recovery, or push fatigue. Two passwords are still one factor category; factor categories include knowledge, possession, and inherence.

**Scenario rule:** Correlate indicators across time, account, device, and source. An alert is a lead; verify before declaring a compromise or blocking a shared service.

### 2.6 Summarize threats and vulnerabilities associated with artificial intelligence usage

**Artificial intelligence (AI)** systems may learn patterns, generate content, or take actions. Their security includes the model, training data, retrieval sources, accounts, tools, and surrounding application.

| Concept | Definition and practical example |
|---|---|
| Model manipulation | Alter model parameters, configuration, or behavior to produce attacker-desired results. A tampered model artifact behaves differently while appearing legitimate. |
| Poisoning | Insert misleading or harmful material into training/fine-tuning data or other trusted data sources. A poisoned knowledge source may encourage wrong security guidance. |
| Prompt injection | Untrusted input attempts to redirect instructions. A document being summarized tells the assistant to export confidential records. Indirect injection comes through retrieved content rather than a user's direct prompt. |
| Data loss | Sensitive information leaks through prompts, output, logs, retrieval, or tool calls. Restrict data access and avoid unnecessary sensitive inputs. |
| Bias | Systematic unfair or skewed results. A model trained on unrepresentative records may misclassify certain groups. |
| Explainability | Ability to understand why an output or decision occurred. Limited explainability makes high-impact decisions harder to audit. |
| Hallucinations | Plausible but false generated statements. A fabricated advisory or command can cause an analyst to make the wrong change. Verify important output against reliable evidence. |
| Jailbreaking | Attempts to circumvent a model's behavioral safeguards. It overlaps with prompt injection, but not every injection is a jailbreak. |
| Evasion | Craft input to avoid detection or produce a wrong classification, such as modifying a malicious sample so a detector misses it. |
| Privacy | Personal information may be collected, retained, inferred, or exposed. Limit collection, access, and retention. |
| Ethical considerations | Assess consent, fairness, accountability, appropriate use, and effects on people. Assign responsibility for decisions and escalation. |
| Session hijacking | Steal or misuse a session to access an AI application, its history, or connected tools. Secure sessions and recheck authorization. |
| Code execution | Generated or attacker-influenced code runs with tool permissions. Sandbox execution, limit privileges, validate parameters, and require appropriate approval for consequential actions. |

**Practical distinction:** Treat retrieved text as data, not authority. Input filters alone are insufficient; independently enforce tool permissions and output validation. See the [Open Worldwide Application Security Project (OWASP) prompt-injection guidance](https://cheatsheetseries.owasp.org/cheatsheets/LLM_Prompt_Injection_Prevention_Cheat_Sheet.html).

## 3.0 Security Architecture — 19%

### 3.1 Compare and contrast security implications of different architecture models

#### Architecture and infrastructure concepts

| Concept | Definition and security implications |
|---|---|
| Cloud | Provider-operated computing services consumed over a network. Customers still manage responsibilities such as identities, data, and configuration; the split depends on the service. |
| Serverless | Provider manages much of the execution infrastructure while customers deploy functions or services. Secure code, permissions, dependencies, and event triggers; servers still exist. |
| Multicloud | Use services from multiple cloud providers. It can reduce some dependencies but increases identity, monitoring, and policy complexity. |
| Hybrid deployment | Combine distinct environments, often on-premises/private resources and public cloud. Secure the connections and ensure consistent identity and visibility. |
| Private deployment | Cloud dedicated to one organization. Greater control does not automatically mean better security; skilled administration is still necessary. |
| Public deployment | Provider services offered to multiple customers with logical isolation. Avoid public exposure caused by customer-side permission errors. |
| Community deployment | Cloud shared by organizations with common requirements, such as a sector's governance needs. Define shared responsibilities and isolation. |
| Infrastructure as Code (IaC) | Define infrastructure through machine-readable, versioned configuration. Review changes, scan configurations, control secrets, and detect drift from approved definitions. |
| OT | Physical-process systems require safety, uptime, and controlled change. Older equipment may not tolerate ordinary scanning or patch schedules. |
| On-premises infrastructure | Organization-operated facilities and systems. Provides direct control but requires physical security, maintenance, power, staffing, and recovery planning. |
| Air-gapped network | Intentionally lacks a network connection to other networks. Removable media, maintenance laptops, and people can still cross the boundary. |
| Microservices | Small, separately deployed services communicate over defined interfaces. Many identities, interfaces, dependencies, and secrets must be secured. |
| Logical segmentation | Separate systems through software-enforced boundaries on shared infrastructure. Access rules can isolate a guest network from internal resources. |
| Physical segmentation | Separate through distinct physical equipment or links. Strong separation can cost more and complicate operations. |

#### Technical considerations

| Consideration | What to evaluate |
|---|---|
| Availability | Can authorized users access the service when required? Identify single points of failure. |
| Resilience | Can the environment withstand or adapt to failures and attacks while maintaining acceptable operation? |
| Proprietary vs. open source | Proprietary software relies on vendor support and licensing; open source offers inspectability and community development. Either can be secure or insecure; evaluate maintenance and supply-chain quality. |
| Usability | Can people reliably use security controls? Unusable workflows can encourage unsafe workarounds. |
| Responsibility | Who patches each component, secures identities, restores data, and investigates alerts? Document the split. |
| Compute | Processing and memory capacity for normal load and security functions, such as encryption or inspection. |
| Power requirements | Electrical needs, backup runtime, cooling, and dependence on the facility. |
| Ease of recovery | How quickly a system can be rebuilt, restored, and verified, including keys and dependencies. |

#### Business considerations

**Data sovereignty:** Data may be subject to rules tied to jurisdiction and control. **Data classification:** Sensitivity determines suitable placement and safeguards. **Cost:** Include licensing, staffing, migration, security, outages, and exit costs. **Ownership:** Clarify who controls assets and data and who is accountable. **Environmental requirements:** Cooling, space, humidity, power, and physical hazards constrain placement. **Scalability:** Ability to handle growth without weakening controls. **Risk:** Compare likely harm, dependencies, and residual exposure, not just convenience.

**Scenario:** A hospital's control equipment may favor an isolated, carefully maintained architecture, while a public information site may favor elastic cloud hosting. Business requirements determine the tradeoffs.

### 3.2 Given a scenario, manage the security architecture to best protect the infrastructure

#### Infrastructure considerations

- **Device placement:** Put controls where they can inspect or enforce the relevant traffic. A firewall cannot protect a path that bypasses it.
- **Security zones:** Group resources by sensitivity and trust requirements; mediate traffic between zones. Public-facing services should not freely reach sensitive databases.
- **Attack surface:** Reduce unnecessary interfaces, services, permissions, and external exposure.
- **Diversity:** Different platforms or implementations can reduce common-mode failure, but they increase administration and testing effort.

#### Zero Trust architecture

**User authentication** verifies the identity requesting access. **Device management** combines **health** checks (patches, protective software, configuration) and **inventory** (known ownership and device records). **Application access control** grants narrowly scoped access to particular applications rather than assuming all network access is trusted. Example: an authenticated user on an unhealthy device may be denied sensitive application access even while on-site.

#### Secure communication/access

| Concept | Definition and example |
|---|---|
| VPN | An authenticated, encrypted connection across an untrusted network. Restrict destination access; a tunnel does not make a compromised endpoint safe. |
| Remote access | Access from outside the local environment. Authenticate users/devices, log sessions, and limit permissions. |
| Tunneling | Encapsulate one protocol within another. Encryption depends on the selected tunnel protocol; encapsulation alone is not confidentiality. |
| User management | Create, update, disable, and review identities and access throughout their life cycle. |
| User access; least privilege | Permit only required resources/actions, with context and duration limits. Separate routine work from privileged administration. |
| End-to-end encrypted messaging | Only intended communicating endpoints can decrypt message contents. Metadata and compromised endpoints can remain exposed. |
| Out-of-band management | A separate management path, ideally isolated from production traffic. Helps administer a failed device but must be strongly protected. |
| File transfer | Move files with authentication, encryption, integrity checks, and appropriate destination permissions. Avoid exposing credentials or leaving unrestricted download links. |
| Security Service Edge (SSE) | Cloud-delivered security capabilities for access to web, cloud, and private applications. Assess identity integration, data handling, provider dependence, and policy consistency. |

#### Identity management and failure modes

- **Group Managed Service Accounts (gMSAs):** Managed domain service identities with automated password handling for supported services. Limit where they can be used and what they can access.
- **Least privilege access accounts:** Dedicated accounts with only required privileges, often separated from ordinary user identities.
- **Privilege creep:** Permissions accumulate as responsibilities change without old access being removed. Periodic access reviews and role changes should remove obsolete rights.
- **Failure modes:** **Fail-open** allows access when a control fails, favoring availability but risking exposure. **Fail-closed** denies access, favoring restriction but risking outage. **Fail-safe** means transition to a state appropriate for safety; it is not always identical to fail-closed. A life-safety exit may unlock while a secure database denies connections.

### 3.3 Summarize concepts and strategies used to protect data

#### Data types and states

| Concept | Definition and example |
|---|---|
| Structured | Data in a defined schema, such as database rows and columns. |
| Unstructured | Data without a uniform tabular schema, such as emails, documents, images, and recordings. |
| Data at rest | Stored data: disks, backups, database files. Use storage encryption and access restrictions. |
| Data in use | Data being processed, often in memory. Restrict execution access and protect processing environments; disk encryption alone does not cover it. |
| Data in transit | Data moving over a connection. Use authenticated secure transport and validate endpoints. |

#### Data classifications

Classification labels are policy-specific and are not a universal single ordered ladder.

| Label | Typical meaning/example |
|---|---|
| Sensitive | Disclosure or misuse could harm people or the organization; customer records. |
| Secret | A formal high-sensitivity category in some classification schemes. Apply the specified access and handling rules. |
| Critical | Essential to operations; loss or corruption has serious consequences. A critical service's data may also be confidential. |
| Confidential | Access limited to authorized parties; internal contracts or personnel information. |
| Public | Approved for unrestricted disclosure; published marketing material still needs integrity protection. |
| Top secret | Very high-sensitivity category in certain formal schemes, requiring stringent handling. |
| Restricted | Closely limited access, often to named roles or groups. The exact ranking depends on policy. |

#### Methods used to secure data

| Method | Definition and example |
|---|---|
| Masking | Hide part or all of a value in a display or test copy. Show only the last four digits of an account number. Underlying originals may still exist. |
| Hashing | Create a digest for integrity checking or comparison. Hashes of low-entropy personal values can still be guessed; hashing is not automatic anonymization. |
| Filtering | Allow, reject, or redact data according to rules. Prevent a sensitive field from being returned to an unauthorized user. |
| Tokenization | Replace sensitive data with a surrogate token and protect the mapping. A payment application stores a token rather than the original card number. |
| Encryption | Transform content using keys; authorized decryption recovers the original. Protect keys separately from data. |
| Data transpose | The PDF does not define this term. In its data-protection context, a reasonable interpretation is rearranging/shuffling data values or positions to obscure associations. Do not assume ordinary matrix transposition or simple rearrangement provides encryption or reliable anonymization. |
| Deidentification | Remove or transform identifying information to reduce linkage to individuals. Assess reidentification from remaining fields and external data. |
| Obfuscation | Make content less readily understandable. Useful for reducing casual disclosure, but strength varies greatly. |

#### Data protection roles

| Role | Typical responsibility |
|---|---|
| Data owner | Accountable business authority deciding classification, acceptable use, and access. |
| Data custodian | Implements storage, backup, permissions, and technical protection. |
| Data steward | Maintains quality, definitions, appropriate use, and governance practices. |
| Data operator | Performs authorized processing or operational handling; exact duties are organization-specific. |
| Data controller | Determines purposes and means of personal-data processing in applicable privacy frameworks. |
| Data subprocessor | Another processor engaged to handle data on behalf of a processor; oversight extends down the chain. |

#### Data handling

**Endpoints:** Control local copies, downloads, caches, and removable storage. **Marking and labeling:** Attach classification metadata or visible markings to support handling rules. **Geofencing:** Restrict actions based on geographic boundaries; location signals can be imperfect. **Data location:** Where data physically or logically resides, including replicas and backups. **Data placement:** The decision to put particular data in particular storage or environments with suitable controls. Location is a fact; placement is an architectural choice.

#### Data management life cycle

1. **Creation:** Minimize collection and assign ownership/classification.
2. **Management:** Control access, accuracy, storage, and protection while maintained.
3. **Distribution:** Share only with authorized recipients using approved methods.
4. **Retention:** Keep data for the required purpose and period; account for holds and backups.
5. **Disposal:** Securely remove or destroy data and verify the result when required.

#### Data compliance

**Standards** set applicable control expectations. **Health data**, **personal information**, **financial data**, and **child/minor data** may have heightened handling requirements. **Intellectual property** needs protection against unauthorized disclosure and use. **Legal data** may require confidentiality, evidence preservation, or restrictions. Requirements depend on jurisdiction, sector, contracts, and data type; classification alone does not establish all obligations.

### 3.4 Explain the importance of resilience and recovery in security architecture

#### Site considerations

| Site/concept | Meaning and tradeoff |
|---|---|
| Hot | Equipped and ready for rapid service restoration, often with current replicated data. High cost and synchronization requirements. |
| Cold | Basic space/utilities; equipment and data must be installed/restored. Lower ongoing cost, slower recovery. |
| Warm | Partially equipped and configured; some restoration and preparation remain. Between hot and cold in readiness and cost. |
| Environmental | Evaluate geographic separation, floods, storms, fire, utilities, cooling, and shared hazards. Two sites on the same floodplain may fail together. |

#### Platform diversity

**Vendor platform diversity** reduces dependence on one vendor's faults or compromise. **Hardware diversity** limits common equipment defects. **Virtualization diversity** can avoid a shared hypervisor weakness but adds operational complexity. Diversity helps only when failure dependencies are genuinely separated.

#### Redundancy strategies and solutions

| Concept | Definition and example |
|---|---|
| Load balancing | Distribute requests across resources. Health checks avoid directing work to failed instances. |
| Clustering | Coordinate multiple nodes to provide a service, using designs such as active-active or active-passive. |
| Autoscaling | Adjust resource count/capacity with demand. Set cost and capacity limits; scaling does not cure all application bottlenecks. |
| High availability | Design to minimize interruption through redundancy and failover. It does not replace backups. |
| Multicloud systems | Use multiple providers to reduce some outage exposure. Shared identity or network dependencies may still fail together. |
| Uninterruptible power supply (UPS) | Short-term battery power and conditioning; supports continued operation or graceful shutdown. |
| Redundant power supply (RPS) | A second power supply path for equipment. Connect to independent feeds where appropriate; two supplies on one circuit share a failure point. |
| Power generator | Longer-duration backup generation requiring fuel, maintenance, and safe transfer. |
| Surge protector | Limits voltage spikes; does not provide outage runtime. |
| Storage | Protect availability and integrity with suitable redundancy, replication, capacity, and access controls. Redundancy can copy corruption or deletion, so it is not a backup. |

#### Backups and testing

| Concept | Definition and example |
|---|---|
| Retention | How long backup versions are preserved. Keep versions old enough to recover from delayed discovery of corruption. |
| Immutability | Prevent alteration/deletion during a protected period. Separate backup administration from compromised production accounts. |
| Scope | Which systems, files, configuration, keys, identities, and dependencies are backed up. Data alone may not rebuild a service. |
| Restoration testing | Actually restore and validate usability, integrity, and timing. A successful backup job is not proof of recoverability. |
| Failover testing | Move service to an alternate component/site and verify access and data consistency. |
| Simulation | Rehearse failure scenarios in controlled conditions to test decisions and procedures. |
| Parallel processing | Run an alternate recovery environment alongside normal operations and compare results without fully cutting over. |

**Disaster recovery** restores affected technology and services after a major disruption. **Business continuity** sustains essential business operations, potentially through manual workarounds. **Capacity planning** ensures processing, storage, network, power, and staffing can support ordinary and recovery workloads.

#### Recovery metrics

| Metric | Definition and example |
|---|---|
| Recovery time objective (RTO) | Target maximum time to restore service after disruption. A two-hour RTO demands a restoration design that can meet two hours. |
| Recovery point objective (RPO) | Target maximum tolerable data loss measured in time. A 15-minute RPO requires recovery data sufficiently recent to meet that objective. |
| Mean time to repair (MTTR) | Average repair duration; measured operational performance, not the recovery target itself. |
| Mean time between failures (MTBF) | Average operating interval between failures for repairable systems. Higher values generally indicate fewer failures, not faster repair. |

**Exam distinction:** RTO asks “How long can we be down?” RPO asks “How much recent data can we lose?” Replication improves recency but can replicate destructive changes.

## 4.0 Security Operations — 27%

### 4.1 Given a scenario, apply mitigating controls, techniques, and solutions to secure the environment

#### Core controls

**Segmentation** limits reachability and lateral movement. **Access controls** enforce who/what can perform which actions. **Hardening** removes unnecessary functionality and secures configuration. **Sandboxing** isolates untrusted code for constrained execution or analysis; it is not a guarantee that escape is impossible.

#### Deception and disruption technology

| Concept | Definition and example |
|---|---|
| Honeypot | Decoy system intended to attract or reveal suspicious interaction. Isolate it so it cannot become an attack platform. |
| Honeynet | A network of decoy systems simulating an environment. |
| Honeyfile | Decoy file that alerts on unexpected access, such as a fake sensitive spreadsheet. |
| Honeytoken | Decoy credential, identifier, or data item whose use signals suspicious activity. |
| Canary account | Account not intended for normal use; attempted authentication or access can trigger an alert. Avoid giving it dangerous permissions. |

**Monitoring/alerting** observes state and behavior, then notifies responders of important events. **Mobile device management (MDM)** centrally enforces settings, inventory, update requirements, and permitted remote actions on enrolled devices. **Application control** uses **allow lists** to permit approved software or **block lists** to reject prohibited software; allow lists require maintenance but limit unknown execution.

#### Intrusion detection/prevention systems

An **intrusion detection system (IDS)** identifies suspicious activity and alerts. An **intrusion prevention system (IPS)** can act to block it.

| Variant | Location and role |
|---|---|
| Network-based intrusion detection system (NIDS) / network-based intrusion prevention system (NIPS) | Inspect traffic at network observation/enforcement points. Encryption and traffic placement affect visibility. |
| Host-based intrusion detection system (HIDS) / host-based intrusion prevention system (HIPS) | Observe or prevent activity on an endpoint, such as file changes or suspicious process behavior. |
| Wireless intrusion prevention system (WIPS) | Detect and, where appropriately configured and authorized, counter wireless threats such as rogue access points. |

Detection without blocking avoids some disruption; prevention requires careful tuning to avoid blocking legitimate activity.

#### Firewalls

| Concept | Definition and example |
|---|---|
| Rate-limiting requests | Restrict request frequency to reduce abuse. Set limits appropriate to user/service behavior; distributed attacks can bypass simple per-address limits. |
| Web application firewall (WAF) | Inspect web requests for application attacks. Useful as a layer, but it does not repair vulnerable application code. |
| Rule-based | Permit or deny traffic using ordered conditions. Understand evaluation order and default action. |
| Unified threat management (UTM) | Combines multiple security functions in one product. Simplifies administration but may concentrate failure and performance risk. |
| Layer 4 / Layer 7 | Layer 4 decisions focus on transport context such as ports and connection state; Layer 7 understands application content/protocols. Decryption may be needed to inspect protected application contents. |

#### Content filters and endpoint security

| Control | Definition and example |
|---|---|
| Content filter | Restricts content, destinations, or categories, such as malicious sites. |
| Data loss prevention (DLP) | Detects and controls prohibited handling or transfer of sensitive data. Rules may inspect content, labels, destinations, or behavior. |
| Agent-based | A component on the device enforces policy or collects data, including some off-network activity. |
| Centralized proxy | An intermediary applies policy to traffic routed through it. Traffic bypassing it may escape inspection. |
| Endpoint detection and response (EDR) | Collects endpoint behavior and supports detection, investigation, and actions such as isolation. |
| Extended detection and response (XDR) | Correlates signals and response across multiple domains, such as endpoints, identity, email, and cloud. Scope varies by product. |
| Antivirus | Detects or blocks malicious software using signatures and other analysis. It is one layer, not complete endpoint defense. |

#### Network access control

**Captive portals** require a browser interaction before access, commonly on guest networks; a checkbox alone does not establish strong device trust. **802.1X** is a port-based access-control standard using an endpoint supplicant, an authenticator such as a switch/access point, and an authentication server. **Endpoint posture/compliance** checks patch state, protective software, enrollment, or configuration before granting or limiting access.

#### Repositories and application security

- **Secrets scanning:** Detect keys/passwords in repositories and their history. If exposed, revoke/rotate the secret; removing the line is insufficient.
- **Input validation:** Accept only expected data types, formats, ranges, and lengths. Combine with safe query/command construction; validation alone does not solve all injection.
- **Secure cookies:** Apply appropriate flags and scope: `Secure` restricts transport to secure connections, `HttpOnly` limits script access, and `SameSite` helps reduce cross-site request abuse. None makes a stolen session harmless.
- **Static code analysis:** Inspect code without running it to identify possible flaws. Review findings because both missed issues and false positives occur.
- **Code signing:** Verify publisher/key identity and that signed content has not changed. A valid signature does not prove code is benign if the signer or signing process is compromised.

#### Email security

| Technology | Definition and distinction |
|---|---|
| Domain-based Message Authentication, Reporting, and Conformance (DMARC) | Uses alignment of the visible sender domain with authenticated sender information and publishes handling/reporting policy. |
| Sender Policy Framework (SPF) | Authorizes sending systems for a domain used in the mail envelope; forwarding can complicate checks. |
| DomainKeys Identified Mail (DKIM) | Uses a domain-associated signature to verify signed message content and domain responsibility. |
| Brand Indicators for Message Identification (BIMI) | Supports display of a verified brand indicator under applicable authentication and provider requirements. It is not a replacement for authentication or content analysis. |

These controls reduce certain forms of domain spoofing; lookalike domains and compromised real accounts can still send convincing phishing messages.

#### Operating systems security

**Group Policy** centrally applies configuration in supported Windows environments, such as account and device restrictions. **Security-enhanced Linux (SELinux)** enforces mandatory access controls through policy and labels, potentially restricting a compromised process beyond ordinary file permissions.

### 4.2 Explain the security implications of proper hardware, software, and data asset management

| Stage/concept | Definition and security purpose |
|---|---|
| Asset management life cycle | Track assets from planning through disposal, including ownership, configuration, use, and risk. Unknown assets cannot be reliably protected. |
| Planning/scoping | Decide needed capabilities, data handled, boundaries, owners, and security requirements. |
| Acquisition/procurement process | Evaluate suppliers, support, provenance, security features, licensing, and lifecycle costs before purchase. |
| Assignment/accounting | Record who has an asset, its owner, location, and authorized purpose. Distinguish software licenses from installed copies and data ownership from device custody. |
| Monitoring/asset tracking | Maintain current inventory and detect changes, missing devices, unsupported software, and unauthorized use. |
| Disposal/decommissioning | Remove access and connections, recover licenses, sanitize data according to media and policy, update inventory, and retain required evidence of disposal. |

**Example:** Retiring a laptop also requires revoking associated access, addressing stored data, checking encryption keys and backups, and recording disposition. Deleting ordinary files may leave recoverable data.

### 4.3 Given a scenario, perform tasks associated with vulnerability management

#### Identification methods

| Method | Definition and example |
|---|---|
| Scanning | Automated discovery and checks for weaknesses. Authenticated scans can inspect local state; unauthenticated scans show more of an external view. Validate scope and operational safety. |
| Internet Protocol Address Management (IPAM) | Maintain address allocation and related inventory to help locate assets and identify unknown or inconsistent use. It supports discovery but does not replace vulnerability scanning. |
| Cloud security posture management (CSPM) | Identify cloud configuration risks, policy violations, and exposure across cloud resources. |
| Source code review | Inspect code for design and implementation weaknesses, manually and with tools. It can reveal flaws before deployment. |

#### Prioritization, remediation, and verification

**Severity assessment** evaluates technical seriousness plus exposure, business impact, and exploitation evidence. **Penetration test report review** identifies demonstrated attack paths, combined weaknesses, and affected assets. **Remediation** may patch, reconfigure, replace, remove, restrict access, or fix code. **Verification** confirms the flaw is resolved through rescanning, inspection, or targeted retesting and checks for side effects.

#### Reporting

**Internal reporting** communicates ownership, risk, deadlines, exceptions, and status to relevant teams. **External reporting** follows approved disclosure paths. A **bounty program** authorizes specified research and potentially rewards qualifying findings. **Responsible disclosure policies** define how to report and coordinate remediation; respect scope, preserve necessary evidence, and avoid unnecessary exposure of sensitive data.

**Scenario:** An internet-facing flaw with active exploitation deserves urgent attention. If a patch is not immediately possible, apply an appropriate temporary restriction, record the residual risk and owner, schedule the fix, and verify both measures.

### 4.4 Explain security alerting and monitoring concepts and tools

#### Monitoring computing resources

**Systems:** Watch hosts, resource use, configuration, and processes. **Applications:** Watch authentication, requests, errors, transactions, and dependencies. **Infrastructure:** Watch network, cloud, storage, identity, and management components. Establish a baseline so deviation has context.

#### Activities

| Activity | Purpose and example |
|---|---|
| Log aggregation | Collect logs into a searchable location; synchronize time and preserve source identity. |
| Alerting | Notify on conditions requiring attention, with severity and enough context to act. |
| Scanning | Inspect assets for exposure or vulnerabilities on an approved schedule. |
| Archiving | Preserve older records with controlled access, retention, and retrievability. |
| Reporting | Summarize findings and trends for technical or managerial audiences. |
| Alert tuning | Adjust thresholds, rules, suppression, and context to reduce noise without hiding real threats. Investigate why an alert fires before suppressing it. |

#### Tools

| Tool/concept | Definition and example |
|---|---|
| Benchmarks | Reference configurations or expected security states used for comparison. |
| Agents/agentless | Agents provide local collection/control; agentless methods use remote interfaces or network visibility. Compare coverage, permissions, maintenance, and off-network visibility. |
| Security information and event management (SIEM) | Centralizes and correlates security data for detection, search, reporting, and investigation. Useful results depend on complete, well-parsed data and tuned rules. |
| Antivirus | Malware detection telemetry can support monitoring and response. |
| DLP | Alerts on possible unauthorized sensitive-data handling; investigate context before declaring a leak. |
| Vulnerability scanners | Identify known flaws and configuration concerns, with validation of results. |
| Orchestration | Coordinates tools and actions into a workflow, such as enriching an alert and opening a case. |
| Packet analyzer | Inspects captured traffic contents and protocol behavior where visible. Encrypted payloads may remain opaque. |

#### Protocols and supporting capabilities

| Concept | Definition and distinction |
|---|---|
| NetFlow | Summarizes network conversations, such as endpoints, ports, duration, and byte counts. Usually not full packet content. |
| Simple Network Management Protocol (SNMP) | Retrieves/manages device information and sends notifications. Prefer authenticated and encrypted versions/configuration where supported. |
| syslog | A standard approach to transporting event messages. Protect transport and collectors; plaintext unauthenticated delivery can expose or distort logs. |
| Security Content Automation Protocol (SCAP) | A suite of specifications supporting machine-readable security configuration and vulnerability information. |
| Automated alerts | Rule- or analytics-generated notifications. Include ownership and escalation so alerts are actually handled. |
| Port mirroring | Copy switch traffic to an observation port for monitoring. Ensure capture capacity and protect the copied data. |
| Dashboards | Visual summaries of status/trends. They depend on underlying data and can hide detail or collection gaps. |
| Network management systems | Monitor device health, availability, configuration, and performance; distinguish operational faults from security events through correlation. |

**Exam distinction:** Flow data explains who talked to whom and how much; packet captures may explain what was exchanged; host logs may reveal which process initiated it.

### 4.5 Given a scenario, apply concepts related to identity and access management

#### Account life cycle and identity

**Provisioning/deprovisioning** creates, changes, and removes accounts/access when people join, move roles, or leave. **Permissions assignments and implications** require correct role, scope, inheritance, and separation of duties. **Identity proofing** establishes a claimed real-world identity before credential issuance; it differs from later authentication. **Federation** lets one identity domain rely on assertions from another.

#### Single sign-on

**Single sign-on (SSO)** lets a user access multiple applications through an established authentication session. It improves usability but concentrates dependence on identity services and session security.

| Technology | Main role and example |
|---|---|
| Security Assertion Markup Language (SAML) | Exchanges signed identity/authentication assertions between an identity provider and a service provider, commonly for enterprise browser sign-in. The PDF says “Assertions”; standard usage is singular “Assertion.” |
| Lightweight Directory Access Protocol (LDAP) | Accesses directory entries such as users/groups; deployments may use it during authentication. It is not interchangeable with browser federation. Secure its transport and permissions. |
| Open Authorization (OAuth) | A delegated authorization framework. An application receives limited access without receiving the user's password. OAuth alone is not a complete authentication protocol. |

#### Account types

| Account | Appropriate purpose and safeguards |
|---|---|
| User | Ordinary personal work; avoid routine administrative privileges. |
| Privileged — global | Broad administrative scope across an environment; strongly restrict, monitor, and separate from daily accounts. |
| Privileged — local | Administrative rights limited to one system; use unique managed credentials to limit lateral movement. |
| Service | Non-human identity for application/service tasks; minimize privileges and manage secrets/lifecycle. |
| Third-party | Vendor/partner access with named ownership, limited scope, expiration, and review. |
| Emergency access | Break-glass access for failure of ordinary access paths; protect, monitor, test, and review its use. |

#### Multifactor authentication methods

**Hard token:** Physical authenticator, such as a security key or code generator. **Soft token:** Software authenticator on a device. **Biometrics:** Inherence-based traits, often used to unlock a device-bound authenticator; assess spoofing and fallback. **One-time password (OTP):** A code valid for one use or a limited interval; codes can be phished. **Backup code:** Recovery secret stored securely and invalidated when used. Recovery paths must not undermine the primary method.

#### Access control models

| Model | Decision basis and example |
|---|---|
| Rule-based | Rules evaluate conditions, such as denying access outside approved network ranges. |
| Role-based | Permissions follow job roles, such as payroll clerk versus payroll approver. |
| Time-based | Access depends on time, such as business hours or a temporary window. |
| Mandatory | Centrally enforced labels/clearances control access; ordinary owners cannot freely override policy. |
| Discretionary | Resource owners can grant access within permitted rules, such as file sharing permissions. |
| Just-in-time | Provide elevated access only when approved and needed, then remove it automatically. |

#### Access management and review

**Authentication** validates the presented identity through approved authenticators. **Logical/technical policies** enforce conditions in systems. **Administrative/business policies** define who should receive access, approval requirements, and conduct. **Access review** verifies rights remain appropriate and removes unnecessary permissions; compare actual access with current responsibilities rather than simply confirming that accounts exist.

#### Password concepts

| Concept | Definition and practical implication |
|---|---|
| Passkey | Public-key credential bound to a service, often unlocked with a device biometric or local secret. The server does not store a reusable shared password for that credential. Protect synchronization and recovery paths. |
| Password managers | Generate/store unique credentials and reduce reuse. Protect the vault and recovery process. |
| Passwordless | Authenticate without a traditional reusable password, for example with a passkey. It can still require local user verification. |
| Length | Longer unpredictable passwords/passphrases resist guessing better than short predictable ones. |
| Complexity | Character-mix rules do not automatically produce unpredictable passwords; predictable substitutions provide limited benefit. |
| Reuse | One breach can expose multiple accounts when passwords are reused. Use unique credentials. |
| Expiration | A rule requiring replacement after a period. Understand the scenario's policy; current guidance generally avoids routine forced changes absent compromise. |
| Age | Minimum age can prevent rapid changes used to defeat history rules; maximum age sets expiration. These are policy settings, not proof of security. |
| Compromised credential monitoring | Detect known-exposed passwords or suspicious credential use and trigger appropriate resets/revocation. |
| Account auditing | Review account state, privileges, inactivity, owner, and suspicious usage. |
| Policy report | Summarize actual compliance and exceptions, such as accounts exempt from required controls. |

The [National Institute of Standards and Technology (NIST) digital identity guidance](https://pages.nist.gov/800-63-4/sp800-63b.html) emphasizes blocking known-compromised/common passwords and does not require routine periodic password changes. Distinguish contemporary guidance from a scenario's expressly stated organizational requirements.

### 4.6 Given a scenario, apply automation and orchestration solutions to secure operations

**Automation** executes a task using predefined logic; **orchestration** coordinates multiple tasks and systems. **Scripting** expresses repeatable actions in code. All inherit the permissions and errors of their design.

#### Use cases

| Use case | Example and safeguard |
|---|---|
| User provisioning | Create access from approved role information; verify ownership and remove access when roles change. |
| Resource provisioning | Deploy systems from approved templates; enforce tags, configuration, and scoped identities. |
| Desired state management | Detect/correct drift from an approved configuration. Avoid repeatedly overwriting justified emergency changes without review. |
| Anomaly detection | Flag behavior deviating from a baseline; account for legitimate seasonal or workload changes. |
| Ticket management | Create, enrich, assign, and track cases automatically; prevent duplication and preserve evidence. |

#### Considerations

**Guardrails:** Bound permissions, action scope, rates, and approvals. **Automation logic:** Test conditions, error handling, retries, and idempotency (safe repeated execution). **Process engineering:** Understand and improve a workflow before automating it. **Complexity:** More dependencies create more failure paths. **Financial:** Compare build, licensing, maintenance, and failure costs against benefits. **Process risks:** Bad logic can spread a mistake rapidly. **Deployment:** Pilot, monitor, version, and provide rollback or a safe stop.

#### Artificial intelligence capabilities

| Capability | Definition and application |
|---|---|
| Agentic | Pursues an objective through tool use and multiple steps. Constrain authority and require suitable checks before consequential actions. |
| Chatbot | Conversational assistance, such as explaining alerts. Validate answers against evidence. |
| Predictive analysis | Estimate future events from patterns, such as likely capacity exhaustion. Uncertainty and changing conditions matter. |
| AI-augmented baselines | Learn expected behavior from data and highlight deviations. Poor or poisoned baseline data can conceal attacks or increase noise. |

#### Intended outcomes, security operations, and workflows

**Efficiency/time saving** reduces repetitive effort. **Enforcing baselines** makes configuration consistent. **Continuous improvements** use feedback to refine processes. **Productivity improvements** let analysts handle higher-value work. **Reduced downtime** comes from faster safe response. **Increased proactivity** identifies issues before they become incidents. Measure these outcomes rather than assuming automation delivers them.

**Security operations (SecOps)** combines security and operational activities. **Continuous integration and continuous deployment (CI/CD)** automates building, testing, and delivery; protect repositories, dependencies, secrets, and pipeline identities. **Workflows** connect triggers, decisions, actions, and results. **Integrations** connect systems through authorized interfaces with limited credentials, validation, and logging.

**Example:** A suspicious sign-in triggers enrichment, a ticket, and analyst review. Automatic account disabling should have confidence thresholds and safeguards because a false positive can disrupt critical operations.

### 4.7 Summarize concepts associated with incident response activities

Incident response is coordinated handling of security events to reduce harm, preserve evidence, restore services, and improve defenses. Stages may overlap and repeat.

#### Preparation

**Training** builds required skills. **Testing** confirms plans and capabilities. **Tabletop exercises** discuss a scenario and decisions without executing a full technical response. **Playbooks** specify actions for particular incident types. **Simulation** rehearses behavior in realistic controlled conditions. **Roles** assign decision authority, technical tasks, evidence custody, and communication responsibility.

#### Identification

**Detection** recognizes potential incidents from telemetry/reports. **Internal advisory** warns relevant staff about observed threats or necessary actions. **External advisory** provides information from vendors, public bodies, or partners. **Threat hunting** proactively searches for adversary behavior not already identified by alerts. Validate scope and severity before choosing response steps.

#### Investigation

| Concept | Meaning and practice |
|---|---|
| Digital forensics | Collect and analyze digital evidence using defensible methods to reconstruct events. |
| Chain of custody | Document evidence identity, collection, transfers, possession, and handling. A hash supports integrity but does not replace custody records. |
| E-discovery | Identify, preserve, collect, review, and produce electronically stored information for legal processes. Coordinate with legal staff. |
| Preservation | Protect evidence against alteration or loss. Capture volatile data when appropriate, use validated methods, and document actions. |

#### Containment, negotiation, eradication, and recovery

**Quarantine/isolation** limits spread while retaining a controlled environment for investigation; choose host, account, network, or application restrictions based on the incident. Powering off can destroy volatile evidence, while leaving a system connected can permit harm; follow the response plan and assess urgency.

**Negotiation** may arise in extortion or crisis handling. It requires designated authority and coordinated legal/business decisions; it is not an ordinary analyst's unilateral action.

**Eradication** removes malware, persistence, exploited weaknesses, and attacker access. **Recovery** restores trusted service, validates integrity, and monitors for recurrence. Restoring a backup without fixing the entry point risks reinfection.

#### Notification/external reporting

**Stakeholders** need timely relevant status and decisions. **Customers** may need protective actions or incident information. **Law enforcement** engagement depends on incident and organizational process. **Mandatory reporting** follows applicable legal, contractual, or regulatory requirements and deadlines; coordinate content and timing with authorized staff.

#### Post-incident

**Lessons learned** identify what worked and what should improve. **Root cause analysis** investigates why the event happened and why controls failed. **Post-incident reporting (PIR)** records timeline, scope, impact, response, recovery, and assigned improvements. Avoid ending with “user clicked a link” when systemic safeguards also failed.

### 4.8 Given a scenario, use data, artifacts and sources to support a security investigation

#### Log and trace data types

| Type | Evidence it may provide |
|---|---|
| Access and accounting — logical | Resource access, actions, and session usage attributed to an identity. |
| Access and accounting — physical | Badge entry, visitor records, and door events. Correlate with logical activity. |
| Device | Router, firewall, appliance, or hardware events and configuration changes. |
| Server | Service starts/stops, system errors, administrative actions, and host events. |
| Application | Requests, transactions, errors, and application-specific actions. |
| Authentication | Successful/failed sign-ins, factor checks, identity changes, and source context. |
| Communication | Message headers, delivery paths, connection events, and communication timing. |
| Audit | Security-relevant actions, permission changes, and administrative operations. |
| Endpoint | Processes, file activity, device connections, and local detections. |
| Network | Connections, traffic volumes, blocked requests, and routing events. |
| Metadata | Context such as sender, recipient, timestamps, sizes, paths, and identifiers; can be informative even when content is encrypted. |

#### Data sources

| Source | Use and limitation |
|---|---|
| Vulnerability scans | Show possible entry weaknesses and affected systems, but not necessarily actual exploitation. |
| Automated reports | Summarize detections and compliance; verify against underlying records. |
| NetFlow / Internet Protocol Flow Information Export (IPFIX) | Analyze communication patterns and volumes; generally not full payload contents. |
| Surveillance footage | Corroborate physical activity and timing; consider coverage and clock offsets. |
| Security tools | Provide alerts, endpoint telemetry, configuration, and response histories. |
| Dashboards | Identify trends and affected areas; drill down to raw evidence. |
| Packet captures | Preserve observable network exchanges; encryption and capture location limit content visibility. |

#### Integrity and system images

**File/log integrity:** Compare trustworthy cryptographic hashes, protect originals, record handling, and use controlled copies for analysis. Logs can be missing or attacker-modified; corroborate independent sources.

| Artifact | Definition and distinction |
|---|---|
| Memory dump | Capture of memory contents; may include running processes, keys, sessions, and volatile artifacts absent from disk. |
| Bit-level copy | Sector/bit-oriented forensic image that can include unallocated space and deleted-data remnants, depending on acquisition method and medium. |
| Snapshot | Point-in-time system/storage state, often useful for recovery. It may omit memory or unallocated data and is not automatically a complete forensic image. |

#### Stakeholders and log parsing

**Human Resources (HR)** coordinates employment-related matters. **Accounts** may refer to finance/accounting or account administration; the PDF does not clarify. Engage the team relevant to the incident, such as finance for payment fraud. **Legal** advises on preservation, privacy, disclosure, and legal process.

**Log-parsing techniques:** Extract fields, normalize formats, filter events, search patterns, correlate identifiers, deduplicate, and construct timelines. Preserve original logs; record time-zone conversions and clock offsets. A structured parser is more reliable than a text search for complex or multiline records.

**Scenario:** A suspicious download investigation can combine identity logs, endpoint process data, file hashes, flow data, application audit events, and badge records. Distinguish observed facts, reasonable inferences, and unresolved gaps.

## 5.0 Security Program Management and Oversight — 14%

### 5.1 Explain the importance of governance, risk, and compliance artifacts

**Governance** establishes direction, accountability, and oversight. **Risk management** identifies and handles uncertainty and potential harm. **Compliance** demonstrates fulfillment of applicable requirements. Documents make responsibilities and expected practices explicit.

#### Guidelines

Guidelines recommend approaches and usually permit discretion unless adopted as mandatory requirements.

| Artifact | Definition and example |
|---|---|
| Benchmarks | Reference settings or measures to evaluate posture; an approved secure server configuration. |
| Advisories | Notices about threats, vulnerabilities, or recommended action; a vendor's urgent patch announcement. |
| Implementation guides | Instructions for applying a technology, standard, or control in practice. |
| Reference architecture | A reusable model showing components, connections, and control placement. Adapt it to actual requirements. |

#### Standards

Standards specify required details that implement policies.

| Artifact/topic | Definition and example |
|---|---|
| Baselines | Minimum approved configuration or control state; logging enabled and unnecessary services disabled. |
| Passwords | Required credential controls, such as uniqueness and handling of compromised passwords. |
| Physical security | Required facility protections, such as visitor escorting and restricted server-room entry. |
| Request for Comments (RFC) | A publication series for internet specifications and related material. Some RFCs are standards; others are informational or experimental. Consult the relevant status and adopted requirements. |
| Encryption | Required protection, approved algorithms/protocols, key management, and exceptions. |

#### Procedures and plans

**Standard operating procedure (SOP):** Approved repeatable steps for an operational task. **Runbook:** Detailed execution instructions for a particular task or condition, often including commands, decision points, and escalation. **Business continuity plan:** How essential business functions continue during disruption. **Disaster recovery plan:** How technology and dependencies are restored. Plans define coordinated action; procedures explain specific execution.

#### Policies

| Policy | What it governs |
|---|---|
| Bring your own device (BYOD) | Use of personally owned devices, enrollment, access, security, privacy, and removal of business data. |
| Acceptable use policy (AUP) | Permitted/prohibited use of organizational systems and resources. |
| Clean desk | Securing unattended sensitive papers, media, and screens. |
| Information security | Organization-wide security expectations, responsibilities, and oversight. |
| Incident response | Reporting, authority, escalation, and coordinated handling of incidents. |
| Data classification and retention | Sensitivity labels, handling requirements, retention periods, and exceptions/holds. |
| Access control | Eligibility, approval, least privilege, review, and removal of access. |
| Data disposal | Authorized sanitization/destruction and verification requirements. |
| Vulnerability disclosure | Channels, scope, researcher expectations, and coordination for reported weaknesses. |
| Privacy | Appropriate personal-data collection, processing, access, sharing, and retention. |

**Exam distinction:** Policy says what/why; standard specifies mandatory details; procedure says how; guideline recommends. An organization can adopt a guideline as a mandatory standard.

### 5.2 Explain the impact of risk management processes on the security of the organization

#### Risk identification and assessment

**Asset identification** records valuable systems, data, people, processes, and dependencies. **Stakeholder ownership** assigns accountable business owners. **Scoring** uses an agreed method to compare risks. **Categorization** groups risks, such as operational, security, financial, and compliance, so appropriate owners can respond.

#### Risk analysis

| Concept | Meaning and application |
|---|---|
| Impact | Magnitude of harm if the event occurs; consider confidentiality, integrity, availability, safety, and business consequences. |
| Likelihood/probability | Chance of occurrence over a stated period, informed by exposure and threat conditions. |
| Owner | Person accountable for treatment decisions, review, and escalation. |
| Current mitigations | Existing controls that change likelihood or impact; validate their effectiveness. |
| Qualitative | Uses descriptive categories such as low/medium/high; practical when precise data is unavailable. |
| Quantitative | Uses numeric estimates, often monetary loss and frequency; useful but depends on assumptions and data quality. |

#### Risk register

A **risk register** records risks, assets, causes, likelihood, impact, controls, owners, treatment, deadlines, and status. **Communication** makes decisions and obligations visible to the right stakeholders. **Reviews** update the register when threats, systems, controls, or business priorities change. A forgotten register does not manage risk.

#### Risk treatment

| Treatment | Definition and example |
|---|---|
| Transferring | Shift some financial/contractual consequences through insurance or agreements. Responsibility and residual exposure do not necessarily disappear. |
| Accepting | Authorized decision to retain a known risk, with rationale, owner, and review conditions. Ignoring a problem is not documented acceptance. |
| Avoiding | Stop the activity creating the risk, such as retiring an unnecessary exposed service. |
| Mitigating | Reduce likelihood or impact through controls, such as segmentation and stronger authentication. |

#### Business-level considerations

| Concept | Definition and example |
|---|---|
| Business impact analysis | Determine critical processes, dependencies, and consequences of disruption to set recovery priorities. |
| Risk appetite | Amount/type of risk leadership is willing to pursue or retain in achieving objectives. |
| Residual risk | Risk remaining after controls/treatment. It must still be owned and reviewed. |
| Stakeholder involvement | Include business, technical, security, finance, and other relevant perspectives. |
| Management oversight | Leadership approves priorities, resources, and risk decisions at appropriate authority levels. |
| Regulatory | Applicable oversight requirements can constrain available treatments. |
| Legal | Law, liability, contracts, and obligations affect acceptable decisions and evidence needs. |
| Single loss expectancy (SLE) | Estimated loss from one occurrence. Common calculation: asset value × exposure factor (fraction lost). |
| Annualized rate of occurrence (ARO) | Estimated frequency per year. One event every four years corresponds to 0.25 per year. |
| Annualized loss expectancy (ALE) | Estimated annual loss: SLE × ARO. It is an estimate, not a guaranteed yearly bill. |

**Worked example:** A $200,000 asset has an estimated 25% loss per incident. SLE = $200,000 × 0.25 = $50,000. With ARO = 0.4, ALE = $20,000. A control costing $6,000 annually that reduces ARO to 0.1 yields a new ALE of $5,000, or $15,000 estimated loss reduction before considering uncertainty and other effects.

### 5.3 Explain the assessment and management processes associated with third-party risk

Third-party risk extends to suppliers, service providers, subcontractors, and dependencies. Outsourcing a service does not eliminate the organization's accountability.

#### Vendor selection

| Concept | Definition and example |
|---|---|
| Request for proposal (RFP) | Ask vendors to propose a solution, approach, and terms for defined needs. |
| Request for information (RFI) | Gather market/capability information before deciding detailed requirements. |
| Request for quote (RFQ) | Ask for pricing on a relatively well-specified purchase. |
| Expression of interest (EOI) | Invite or submit preliminary interest/capability for an opportunity. |
| Due diligence | Investigate security, finances, reliability, data handling, subcontractors, and support before selection and throughout the relationship. |
| Conflict of interest | Personal or business interests could improperly influence judgment. Disclose and manage them to protect objective selection. |

#### Agreement types

| Agreement | Definition and distinction |
|---|---|
| Service-level agreement (SLA) | Agreement defining service commitments, measurement, responsibilities, and often consequences for failure. |
| Service-level objective (SLO) | Specific measurable target, such as an availability goal; may support an SLA. |
| Memorandum of understanding (MOU) | Documents shared intent or understanding. Enforceability depends on wording and applicable law. |
| Memorandum of agreement (MOA) | Documents agreed responsibilities/commitments, often more specific than an MOU; do not assume legal effect from its title alone. |
| Non-disclosure agreement (NDA) | Governs confidential information use and disclosure. |
| Master services agreement (MSA) | Establishes general terms for an ongoing service relationship. The acronym list says “Master Service Agreement”; the objective uses plural “services.” |
| Statement of work (SOW) | Defines a particular project's scope, deliverables, tasks, and acceptance conditions. |

#### Vendor monitoring

**Right to audit** establishes permitted verification of controls. **Service-level monitoring** compares performance with commitments. **Vendor registry** tracks suppliers, owners, access, data, contracts, and criticality. **Vendor assessment** evaluates changing risk and control effectiveness. **Compliance attestation** is a statement/evidence of compliance within a specified scope and period; inspect limitations. **Penetration testing** demonstrates exploitable paths within authorized scope and should be reviewed alongside remediation evidence.

#### Limitations/constraints and rules of engagement

| Constraint | Security implication |
|---|---|
| Staffing limitations | Limited expertise/time may restrict review or monitoring depth. Prioritize critical vendors. |
| Resource availability | Tools, budget, data, or access may limit assessment. Record assurance gaps. |
| Environment | Shared/cloud/production systems may restrict testing or direct visibility. |
| Legal and regulatory factors | Data handling, testing, contracts, and reporting obligations can limit options. |
| Geography/jurisdiction | Location affects access, legal obligations, and recovery logistics. |
| Financial / return on investment (ROI) | Compare value with costs, including security, transition, and exit costs. A common ROI formula is (benefit − cost) ÷ cost. |
| Vendor lock-in | Dependence on proprietary interfaces, formats, or terms makes switching difficult. Plan data export and exit. |
| Assurance mechanisms | Obtain confidence through reports, tests, certifications, contracts, and ongoing evidence. Each has scope/quality limits. |

**Rules of engagement** define authorized targets, methods, timing, restrictions, communication, evidence handling, and stop conditions for testing. Permission to use a service does not imply permission to attack-test its provider.

### 5.4 Summarize elements of effective security compliance

#### Compliance training and monitoring

| Concept | Definition and example |
|---|---|
| Data handling | Teach applicable classification, access, sharing, retention, and disposal practices. |
| Anti-money laundering/counter-terrorism financing (AML/CTF) | Processes/training to recognize and report suspicious financial activity under applicable obligations. |
| Anti-bribery | Teach prohibited improper inducements, disclosure requirements, and reporting channels. |
| Attestations | Formal statements that requirements are met; support them with verifiable evidence. |
| Acknowledgements | Record that someone received/understood a policy or training. Signing does not prove correct ongoing behavior. |

#### Consequences of non-compliance

**Reputational damage** reduces trust. **Financial consequences** include fines, remediation, and losses. **Legal consequences** include litigation or other proceedings. **Contractual consequences** include penalties or termination. **Sanctions** can restrict activities or impose other penalties. **Loss of license** can remove permission to operate. Applicability depends on the actual requirement and circumstances.

#### Privacy

| Concept | Meaning and practical implication |
|---|---|
| Right to be forgotten | Under applicable frameworks, a right to request erasure subject to conditions and exceptions. It is not an unconditional right to delete every record immediately. |
| Opt-in or opt-out | Consent/choice mechanisms: opt-in requires affirmative agreement; opt-out permits withdrawal from a default arrangement where allowed. |
| Data correction | Fix inaccurate personal information through an appropriate process. |
| Processing restrictions | Limit how data is processed, possibly retaining it without ordinary use while a dispute is resolved. |
| Processing prevention | Stop prohibited processing; the precise legal mechanism depends on jurisdiction and circumstances. |
| Controller vs. processor | Controller determines purposes/means; processor handles data on the controller's behalf. Contracts and duties should reflect actual roles. |
| Ownership | Clarify accountability and rights in data governance. Business “ownership” does not remove individuals' applicable privacy rights. |

#### Legal compliance

**Legal hold** suspends normal disposal for potentially relevant records. **Legal orders** direct preservation, production, restrictions, or other action through applicable legal authority. **Data retention requirements** specify minimum/maximum retention and purpose. Coordinate conflicts between deletion requests and preservation obligations with legal staff; do not assume one label settles the issue.

For the erasure exception concept, see the [European Data Protection Board's explanation of the right to erasure](https://www.edpb.europa.eu/sme/be-compliant/respect-individuals-rights_en). This is a jurisdiction-specific example, not a universal rule for every organization.

### 5.5 Explain concepts associated with audit and assessment activities

#### Data gathering

| Method | Definition and example |
|---|---|
| Sampling | Examine a selected subset to draw conclusions about a larger set. Biased or too-small samples can miss failures. |
| Questionnaires/surveys | Structured responses efficiently collect information but may need verification. |
| Interviews | Ask personnel how processes actually work; compare answers with documents and evidence. |
| Assertion | A claim about control state or performance, such as “all privileged accounts use MFA.” Test the claim. |

#### Reference sources

- **MITRE Adversarial Tactics, Techniques, and Common Knowledge (ATT&CK):** A knowledge base of observed adversary behaviors. Tactics explain why an action is taken; techniques describe how. Map detections and gaps to behaviors, not merely product names. MITRE is an organization name, not a current acronym needing expansion. See [MITRE's resources](https://attack.mitre.org/resources/).
- **Cyber Kill Chain:** A model of reconnaissance, weaponization, delivery, exploitation, installation, command and control, and actions on objectives. It helps identify opportunities to interrupt a campaign. The stages do not perfectly describe every incident. See [Lockheed Martin's model](https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html).
- **Diamond Model of Intrusion Analysis:** Relates adversary, infrastructure, capability, and victim in an intrusion event. Linking common infrastructure or capabilities can help connect events.

#### Scoping

**Audit charter** establishes purpose, authority, responsibilities, and independence. **Frequency** sets how often review occurs based on risk, requirements, and change. Scope should identify systems, locations, time periods, requirements, and exclusions; an audit outside a system's scope says little about that system.

#### Engagement types

| Type | Definition and distinction |
|---|---|
| Gap analysis | Compare present controls with a desired standard or target state to identify missing elements. |
| Internal compliance | Organization evaluates whether applicable requirements are being followed. |
| Audit committee | Oversight body reviewing audit activity, findings, independence, and follow-up. |
| Self-assessments | Teams assess their own practices; useful but vulnerable to bias or insufficient evidence. |
| External examinations | Formal outside scrutiny of specified conditions or records. |
| External assessments | Outside evaluation of security posture, controls, or risk. |
| Regulatory | Review performed for or by an oversight authority under its mandate. |
| Independent third-party audits | External evaluation intended to provide independent assurance within defined scope. |
| Benchmarking | Compare controls/performance with a reference or peers; context matters. |

#### Penetration testing

| Type/concept | Definition and practical distinction |
|---|---|
| Known environment | Tester receives substantial environment information and possibly access; enables depth and efficiency. |
| Unknown environment | Tester receives little internal information; approximates an outsider's discovery challenge. |
| Partially known environment | Tester receives some information or access; balances realism and depth. |
| Physical | Tests facility entry and physical controls within explicit authorization. |
| Offensive | Simulates adversary actions to find and demonstrate exploitable weaknesses. |
| Defensive | Evaluates defenders' detection, investigation, and response capabilities. |
| Integrated | Coordinates offensive and defensive activity to improve controls through shared learning. |
| Passive reconnaissance | Gather information without directly interacting with target systems, such as public records. |
| Active reconnaissance | Interact with target systems, such as approved service discovery. It can be detectable and disruptive. |

A vulnerability scan identifies possible weaknesses; a penetration test attempts to demonstrate exploitability/impact within authorized limits. Neither guarantees all weaknesses are found.

#### Frameworks, standards, and test focus

**Industry-based standards** reflect sector requirements. **International standards** support cross-border consistency. **Region-specific standards** reflect particular jurisdictional expectations. Choose what applies to the organization's activities, scope, and obligations rather than assuming any certification covers everything.

**Functional testing** asks whether a control performs its required function: does an unauthorized request get denied? **Behavioral testing** examines actions under realistic conditions: do staff report suspicious requests and do responders escalate correctly? The PDF does not give narrower definitions; use the scenario's context, including software behavior where relevant.

### 5.6 Given a scenario, apply security awareness concepts to improve organizational security

#### Types of training

| Type | Definition and example |
|---|---|
| Initial/onboarding | Introduce policies, reporting, and safe practices when joining or receiving access. |
| Ongoing | Reinforce and update knowledge over time. |
| Targeted | Tailor to a role or risk, such as payment-fraud training for finance. |
| Corrective | Address an observed error or gap with focused improvement rather than merely blame. |

#### Delivery mechanisms

**Learning management system (LMS)** assigns, tracks, and tests training. **Self-service portals** provide accessible guidance when needed. **One-to-one** instruction supports individual coaching or sensitive issues. **One-to-many** reaches groups efficiently through classes, briefings, or webinars. Choose accessible formats and role-relevant examples.

#### Reporting and monitoring of effectiveness

**Metrics** measure outcomes such as reporting rate, time to report, repeat errors, and appropriate handling. **Managerial reports** summarize trends, gaps, and accountable improvements. **Personnel behavior risk scoring** uses observed patterns to focus assistance; validate data, minimize privacy impact, account for job context, and avoid treating a score as proof of intent. Training completion alone does not demonstrate secure behavior.

#### Common training topics

| Topic | Practical behavior to teach |
|---|---|
| Social engineering | Recognize manipulation, verify requests independently, and report quickly. |
| Emerging security topics | Update staff for changing threats, such as synthetic impersonation or unsafe AI tool use. |
| Password and credential management | Use unique credentials, protect authenticators/recovery codes, and report suspected compromise. |
| Remote work/teleworking/hybrid | Secure devices, home/work connections, screens, physical spaces, and approved remote access. |
| BYOD | Follow enrollment and access rules; understand boundaries between personal and organizational data. |
| Business email compromise (BEC) | Fraud using impersonated or compromised business communications. Verify payment/bank changes through an independently known channel and approval workflow. |
| Removable media and cables | Avoid unknown media and untrusted accessories; some cables/devices can contain attack hardware. |
| Situational awareness | Notice nearby observers, unattended devices, suspicious visitors, and unexpected requests. |
| Operational security | Avoid exposing details that reveal operations, capabilities, schedules, or sensitive plans. A harmless-looking photo may reveal badges or internal screens. |

**Scenario:** For rising payment fraud, train finance on independent callback verification, update approval procedures, measure reporting and verification behavior, and revise training based on results.

## Glossary of important distinctions

This compact glossary supplements the objective tables. Use the objective links for definitions, examples, and context.

### Foundations and cryptography

| Term pair/group | Distinction | Review |
|---|---|---|
| Confidentiality / integrity / availability | Secrecy / trustworthy data state / usable service. | [1.1](#11-explain-security-concepts-and-controls) |
| Authentication / authorization / accounting | Verify identity / decide permissions / record actions. | [1.1](#11-explain-security-concepts-and-controls) |
| Control category / control type | Implementation family / purpose. One control can serve several purposes. | [1.1](#11-explain-security-concepts-and-controls) |
| Backout / fail forward | Restore previous state / repair or complete the new state. | [1.2](#12-given-a-scenario-demonstrate-the-impact-of-change-management-processes-on-security) |
| Encryption / hashing / signing | Hide contents / produce digest / verify signed origin and integrity. | [1.3](#13-explain-the-importance-of-using-appropriate-cryptographic-solutions) |
| Salt / key | Public uniqueness material for password hashing / secret or public cryptographic input with a different role. | [1.3](#13-explain-the-importance-of-using-appropriate-cryptographic-solutions) |
| Certificate / public key | A signed binding containing a key and attributes / the key itself. | [1.3](#13-explain-the-importance-of-using-appropriate-cryptographic-solutions) |

### Threats and vulnerabilities

| Term pair/group | Distinction | Review |
|---|---|---|
| Threat / vulnerability / exploit / risk | Potential harm source / weakness / use of weakness / contextual possibility and consequence of harm. | [2.1](#21-explain-characteristics-of-threats-and-vulnerabilities) |
| Severity / priority | Technical seriousness / remediation order using business and threat context. | [2.1](#21-explain-characteristics-of-threats-and-vulnerabilities) |
| Vector / attack surface | Route into a target / all exposed opportunities. | [2.3](#23-describe-threat-vectors-and-sources), [2.4](#24-explain-types-of-vulnerabilities-and-attack-surfaces) |
| Virus / worm / Trojan | Infects host content / self-propagates / disguises malicious behavior as legitimate. | [2.5](#25-given-a-scenario-analyze-indicators-of-malicious-activity) |
| Spraying / brute force | Few guesses across many accounts / many candidate guesses. | [2.5](#25-given-a-scenario-analyze-indicators-of-malicious-activity) |
| Prompt injection / poisoning / evasion | Redirect through input / corrupt trusted model or data sources / avoid correct detection. | [2.6](#26-summarize-threats-and-vulnerabilities-associated-with-artificial-intelligence-usage) |
| Indicator / proof | Clue needing context / sufficiently supported conclusion. | [2.5](#25-given-a-scenario-analyze-indicators-of-malicious-activity) |

### Architecture and data

| Term pair/group | Distinction | Review |
|---|---|---|
| Hybrid / multicloud | Combine distinct environments / use multiple providers. They can coexist. | [3.1](#31-compare-and-contrast-security-implications-of-different-architecture-models) |
| Logical / physical segmentation | Enforced separation on shared infrastructure / separate physical paths or equipment. | [3.1](#31-compare-and-contrast-security-implications-of-different-architecture-models) |
| Fail-open / fail-closed | Allow on control failure / deny on control failure. | [3.2](#32-given-a-scenario-manage-the-security-architecture-to-best-protect-the-infrastructure) |
| Masking / tokenization / encryption | Hide displayed values / substitute mapped values / cryptographically transform values. | [3.3](#33-summarize-concepts-and-strategies-used-to-protect-data) |
| Owner / custodian / steward | Business accountability / technical handling / quality and governance. | [3.3](#33-summarize-concepts-and-strategies-used-to-protect-data) |
| Hot / warm / cold site | High / intermediate / low recovery readiness. | [3.4](#34-explain-the-importance-of-resilience-and-recovery-in-security-architecture) |
| High availability / backup | Maintain service through failures / recover earlier preserved data. | [3.4](#34-explain-the-importance-of-resilience-and-recovery-in-security-architecture) |
| Recovery time / recovery point | Tolerable restoration delay / tolerable lost-data interval. | [3.4](#34-explain-the-importance-of-resilience-and-recovery-in-security-architecture) |

### Operations and identity

| Term pair/group | Distinction | Review |
|---|---|---|
| Detection / prevention | Observe and alert / block or constrain. | [4.1](#41-given-a-scenario-apply-mitigating-controls-techniques-and-solutions-to-secure-the-environment) |
| Identification / authentication | Claim an identity / verify the claim. Identity proofing establishes real-world identity earlier. | [4.5](#45-given-a-scenario-apply-concepts-related-to-identity-and-access-management) |
| Federation / single sign-on | Cross-domain trust / reuse of an authenticated session across services. | [4.5](#45-given-a-scenario-apply-concepts-related-to-identity-and-access-management) |
| Role-based / rule-based | Job-role membership / evaluated conditions. | [4.5](#45-given-a-scenario-apply-concepts-related-to-identity-and-access-management) |
| Automation / orchestration | Execute tasks / coordinate tasks across systems. | [4.6](#46-given-a-scenario-apply-automation-and-orchestration-solutions-to-secure-operations) |
| Containment / eradication / recovery | Limit harm / remove attacker and causes / restore trusted service. | [4.7](#47-summarize-concepts-associated-with-incident-response-activities) |
| Hash / chain of custody | Integrity comparison / documented evidence handling and possession. | [4.8](#48-given-a-scenario-use-data-artifacts-and-sources-to-support-a-security-investigation) |
| Snapshot / forensic image | Platform-defined point-in-time state / evidence acquisition designed for investigative completeness. | [4.8](#48-given-a-scenario-use-data-artifacts-and-sources-to-support-a-security-investigation) |

### Governance and risk

| Term pair/group | Distinction | Review |
|---|---|---|
| Policy / standard / procedure / guideline | Direction / mandatory detail / execution steps / recommendation. | [5.1](#51-explain-the-importance-of-governance-risk-and-compliance-artifacts) |
| Inherent / residual risk | Risk before controls / risk after controls. Inherent risk is added context for residual risk. | [5.2](#52-explain-the-impact-of-risk-management-processes-on-the-security-of-the-organization) |
| Appetite / acceptance | Broad willingness to retain risk / explicit decision about a particular risk. | [5.2](#52-explain-the-impact-of-risk-management-processes-on-the-security-of-the-organization) |
| Quantitative / qualitative | Numeric estimates / descriptive categories. | [5.2](#52-explain-the-impact-of-risk-management-processes-on-the-security-of-the-organization) |
| Agreement / objective | Contractual service commitment / measurable service target. | [5.3](#53-explain-the-assessment-and-management-processes-associated-with-third-party-risk) |
| Attestation / acknowledgement | Claim of compliance / record of receipt or understanding. | [5.4](#54-summarize-elements-of-effective-security-compliance) |
| Audit / assessment / penetration test | Evidence-based evaluation against criteria / broader evaluation / authorized demonstration of exploitability. | [5.5](#55-explain-concepts-associated-with-audit-and-assessment-activities) |
| Legal hold / retention schedule | Preserve relevant records despite ordinary disposal / routine rules for keeping and deleting records. | [5.4](#54-summarize-elements-of-effective-security-compliance) |

## Complete acronym glossary

The following sections include every entry in the PDF's acronym list, with standard expansions and concise working meanings. Items appearing only in that list remain included. Minor source wording discrepancies are noted rather than taught as incorrect terminology.

### A–C

| Acronym | Full name | Working meaning |
|---|---|---|
| AAA | Authentication, Authorization, and Accounting | Identity verification, permission decisions, and activity recording. |
| AI | Artificial Intelligence | Systems performing tasks such as prediction, generation, or autonomous tool use. |
| ALE | Annualized Loss Expectancy | Estimated yearly loss: single-event loss multiplied by annual frequency. |
| AML/CTF | Anti-money Laundering/Counter-terrorism Financing | Controls addressing illicit money movement and terrorist funding. |
| APT | Advanced Persistent Threat | Sustained, capable adversary activity pursuing long-term objectives. |
| ARO | Annualized Rate of Occurrence | Estimated number of occurrences per year; can be a fraction. |
| AUP | Acceptable Use Policy | Rules for permitted use of organizational resources. |
| BEC | Business Email Compromise | Business-message fraud, often involving payments or account changes. |
| BIMI | Brand Indicators for Message Identification | Brand display mechanism tied to applicable email authentication requirements. |
| BIOS | Basic Input/Output System | Firmware that initializes hardware and begins startup; unauthorized changes can affect system trust. |
| BYOD | Bring Your Own Device | Use of personally owned devices under organizational access/security rules. |
| CAB | Change Advisory Board | Body reviewing changes, risk, timing, and approval requirements. |
| CAPTCHA | Completely Automated Public Turing test to tell Computers and Humans Apart | Human-versus-automation challenge; attackers may abuse fake challenge pages. |
| CI/CD | Continuous Integration and Continuous Deployment | Automated integration, testing, and deployment pipeline; protect its privileges and dependencies. |
| CIA | Confidentiality, Integrity, and Availability | Three foundational goals: secrecy, trustworthy state, and accessible service. |
| CRL | Certificate Revocation List | Published list of certificates revoked before their expiration. |
| CSPM | Cloud Security Posture Management | Checks cloud resources for misconfiguration, exposure, and policy violations. |
| CSR | Certificate Signing Request | Request containing identity details and a public key for certificate issuance. |
| CVE | Common Vulnerabilities and Exposures | Identifier naming a publicly disclosed vulnerability. |
| CVSS | Common Vulnerability Scoring System | Structured technical severity scoring; distinct from organization-specific risk. |
| CWE | Common Weakness Enumeration | Catalog of weakness types, such as unsafe input handling; distinct from a specific vulnerability identifier. |

### D–H

| Acronym | Full name | Working meaning |
|---|---|---|
| DDoS | Distributed Denial of Service | Service exhaustion/disruption from distributed sources. |
| DHCP | Dynamic Host Configuration Protocol | Automatically supplies network configuration; rogue servers can provide malicious settings. |
| DKIM | DomainKeys Identified Mail | Domain-associated signature on email; verifies signed content and domain responsibility. |
| DLP | Data Loss Prevention | Detection/control of prohibited sensitive-data handling and transfer. |
| DMARC | Domain-based Message Authentication, Reporting, and Conformance | Email alignment, policy, and reporting built on sender authentication. |
| DNS | Domain Name System | Maps names to records such as addresses; a target for redirection and tunneling. |
| DoS | Denial of Service | Attack preventing legitimate service use; may involve one or many sources. |
| EDR | Endpoint Detection and Response | Endpoint telemetry, investigation, detection, and response capabilities. |
| EOI | Expression of Interest | Preliminary expression of capability or interest in a procurement opportunity. |
| GBIC | Gigabit Interface Converter | Pluggable network transceiver module; appears in the PDF's equipment/acronym material. |
| gMSA | Group Managed Service Account | Managed service identity with automated password handling in supported domain environments. |
| HIDS | Host-based Intrusion Detection System | Host-local monitoring that detects suspicious activity. |
| HIPS | Host-based Intrusion Prevention System | Host-local control capable of blocking suspicious activity. |
| HR | Human Resources | Employment-related stakeholder in investigations, training, and account lifecycle. |

### I–N

| Acronym | Full name | Working meaning |
|---|---|---|
| IaC | Infrastructure as Code | Machine-readable infrastructure definitions enabling repeatable reviewed deployments. |
| IDS | Intrusion Detection System | Detects suspicious activity and alerts; does not inherently block. |
| IP | Internet Protocol | Network-layer addressing and delivery protocol; address alone is not proof of identity. |
| IPFIX | Internet Protocol Flow Information Export | Standardized export of network-flow information, not necessarily payload contents. |
| IPS | Intrusion Prevention System | Detects and can block suspicious activity; tuning affects false-positive disruption. |
| IPSec | Internet Protocol Security | Suite protecting network traffic, commonly used in secure tunnels. |
| LAN | Local Area Network | Network serving a limited local area; internal location does not imply trust. |
| LDAP | Lightweight Directory Access Protocol | Directory access protocol; protect credentials, queries, and directory permissions. |
| LLM | Large Language Model | Language-generating model with risks including injection, disclosure, and unreliable output. |
| LMS | Learning Management System | Platform assigning, delivering, and tracking training. |
| MDM | Mobile Device Management | Central enrollment, configuration, inventory, and management of mobile devices. |
| MFA | Multifactor Authentication | Authentication using multiple distinct factor categories. |
| MOA | Memorandum of Agreement | Document of agreed responsibilities/commitments; legal effect depends on content and law. |
| MOU | Memorandum of Understanding | Document of shared intent/understanding; do not assume enforceability from title. |
| MSA | Master Services Agreement | General terms governing a continuing service relationship. |
| MTBF | Mean Time Between Failures | Average operating time between failures of a repairable system. |
| MTTR | Mean Time to Repair | Average time to repair; measured performance rather than a recovery target. |
| NDA | Non-disclosure Agreement | Terms limiting use/disclosure of confidential information. |
| NFC | Near-field Communication | Short-range radio communication; proximity alone does not eliminate relay or trust risks. |
| NIC | Network Interface Card | Hardware/network interface connecting a system to a network. |
| NIDS | Network-based Intrusion Detection System | Network-positioned detection of suspicious traffic. |
| NIPS | Network-based Intrusion Prevention System | Network-positioned detection with prevention capability. |
| NVD | National Vulnerability Database | Vulnerability database maintained by NIST, providing vulnerability-related information/enrichment. |

### O–R

| Acronym | Full name | Working meaning |
|---|---|---|
| OAuth | Open Authorization | Delegated authorization framework; not by itself a complete authentication protocol. |
| OCSP | Online Certificate Status Protocol | Protocol to obtain certificate revocation status. |
| OS | Operating System | Software managing hardware, processes, memory, and resources; includes a major security boundary. |
| OT | Operational Technology | Technology monitoring or controlling physical operations, with safety and availability needs. |
| OTP | One-time Password | Authentication code valid for a single use or short period; can still be phished. |
| PDF | Portable Document Format | Document format; malicious files may exploit readers or contain deceptive/active content. |
| PIR | Post-incident Reporting | Post-incident account of evidence, actions, impact, and improvements. |
| PKI | Public Key Infrastructure | Certificates, authorities, keys, and processes establishing public-key trust. |
| QR | Quick Response | Machine-readable code often encoding a destination; verify the destination before acting. |
| RCS | Rich Communication Services | Enhanced mobile messaging; another channel for deceptive messages. |
| RF | Radio Frequency | Radio-frequency communication underlying many wireless interfaces. |
| RFC | Request for Comments | Internet specification/publication series; not every RFC is a standard. |
| RFI | Request for Information | Procurement request gathering vendor/market capability information. |
| RFP | Request for Proposal | Procurement request for proposed solutions and terms. |
| RFQ | Request for Quote | Procurement request for pricing against a specified need. |
| ROI | Return on Investment | Value relative to cost; include security, maintenance, and transition costs. |
| RPO | Recovery Point Objective | Maximum targeted tolerable data-loss interval. |
| RPS | Redundant Power Supply | Redundant device power supply; separate upstream feeds reduce shared failure. |
| RTF | Rich Text Format | Document format that can be used in malicious attachment delivery. |
| RTO | Recovery Time Objective | Maximum targeted restoration delay after disruption. |

### S–X

| Acronym | Full name | Working meaning |
|---|---|---|
| SaaS | Software as a Service | Provider-hosted application service; customer identity/data responsibilities remain. |
| SAML | Security Assertion Markup Language | Framework for exchanging identity/authentication assertions in federation. |
| SCAP | Security Content Automation Protocol | Specifications supporting automated security configuration and vulnerability information. |
| SELinux | Security-enhanced Linux | Linux mandatory-access-control framework using policy and labels. |
| SFP | Small Form-factor Pluggable | Compact pluggable transceiver module; appears in equipment/acronym material. |
| SIEM | Security Information and Event Management | Central collection, correlation, search, and reporting of security events. |
| SLE | Single Loss Expectancy | Estimated loss per incident, often asset value multiplied by exposure fraction. |
| SMS | Short Message Service | Text messaging channel; smishing uses it for deception. |
| SNMP | Simple Network Management Protocol | Network device information/management protocol; secure its version and configuration. |
| SOAR | Security Orchestration, Automation, and Response | Combines security case handling and coordinated automated workflows across tools. |
| SOC | Security Operations Center | Team/function monitoring and responding to security events; here it does not mean an audit-report designation. |
| SOP | Standard Operating Procedure | Approved repeatable operational instructions. |
| SOW | Statement of Work | Project-specific scope, tasks, deliverables, and acceptance terms. |
| SPF | Sender Policy Framework | Domain policy identifying authorized email-sending infrastructure. |
| SQL | Structured Query Language | Language for relational data operations; unsafe query construction can permit injection. |
| SSE | Security Service Edge | Cloud-delivered security for access to web, cloud, and private applications. |
| SSO | Single Sign-on | Reuse of an authentication session to access multiple services. |
| TLS | Transport Layer Security | Authenticated secure transport protocol; certificate validation and configuration matter. |
| TOC | Time-of-check | Point at which an application validates a resource or condition. |
| TOU | Time-of-use | Point at which the resource is actually used; changes since the check may cause a race flaw. |
| UPS | Uninterruptible Power Supply | Battery-backed short-term power for operation or safe shutdown. |
| USB | Universal Serial Bus | Device connection interface; media and device emulation can carry attacks. |
| UTM | Unified Threat Management | Product combining multiple security functions with shared administration. |
| VNC | Virtual Network Computing | Remote screen/desktop control technology requiring protected access. |
| VPN | Virtual Private Network | Protected network connection across another network; endpoint security still matters. |
| WAF | Web Application Firewall | Filter inspecting web application traffic; complements secure application code. |
| WIPS | Wireless Intrusion Prevention System | Wireless threat detection and prevention capability. |
| XDR | Extended Detection and Response | Correlated detection/response across several security domains. |

### Additional acronyms used in this guide or objectives

These are not all included in the PDF's acronym appendix, but appear in the objectives or supporting explanations.

| Acronym | Full name | Working meaning |
|---|---|---|
| ATT&CK | Adversarial Tactics, Techniques, and Common Knowledge | MITRE knowledge base for adversary behavior. |
| IPAM | Internet Protocol Address Management | Maintains address allocation and related inventory. |
| IT | Information Technology | Computing and information systems; shadow IT lacks approved oversight. |
| NIST | National Institute of Standards and Technology | Publishes technical guidance and maintains vulnerability resources. |
| OWASP | Open Worldwide Application Security Project | Community producing application-security guidance, including AI security resources. |
| SecOps | Security Operations | Coordinated security and operational work. |
| SLA | Service-level Agreement | Agreed service commitments, responsibilities, and remedies. |
| SLO | Service-level Objective | Measurable performance target supporting service commitments. |

## Scenario practice and self-checks

These are original learning exercises. Try to explain the reasoning before reading the answer.

| Scenario/question | Answer and reasoning | Objectives |
|---|---|---|
| A visible camera records a server-room door. What category and types apply? | Physical category; detective through recording and deterring through visibility. A control can have multiple functions. | [1.1](#11-explain-security-concepts-and-controls) |
| A database migration cannot safely be reversed after new transactions arrive. What should the change plan address? | A tested fail-forward path, decision authority, dependencies, communication, and recovery criteria. “We will roll back” is inadequate if reversal loses data. | [1.2](#12-given-a-scenario-demonstrate-the-impact-of-change-management-processes-on-security) |
| A signed file is readable. Did signing fail? | No. Signing supports origin/integrity verification; encryption is needed for confidentiality. | [1.3](#13-explain-the-importance-of-using-appropriate-cryptographic-solutions) |
| A severe flaw is isolated, while a less severe flaw is actively exploited on a public payment server. Which gets attention first? | Consider the public exploited flaw first because exposure, exploitation, and business impact can outweigh raw severity. Validate both environments. | [2.1](#21-explain-characteristics-of-threats-and-vulnerabilities), [4.3](#43-given-a-scenario-perform-tasks-associated-with-vulnerability-management) |
| Many users have one failed login with the same common password. What attack pattern fits? | Password spraying; correlate source, timing, and outcomes. | [2.5](#25-given-a-scenario-analyze-indicators-of-malicious-activity) |
| A retrieved document tells an assistant to reveal private records. What is the risk? | Indirect prompt injection. Treat the document as untrusted data and independently enforce tool/data permissions. | [2.6](#26-summarize-threats-and-vulnerabilities-associated-with-artificial-intelligence-usage) |
| A service must return within two hours and lose no more than 15 minutes of data. Which metrics are these? | RTO = two hours; RPO = 15 minutes. Restoration speed and backup/replication recency are different design concerns. | [3.4](#34-explain-the-importance-of-resilience-and-recovery-in-security-architecture) |
| Two power supplies use the same power strip and circuit. Is power failure fully addressed? | No. Device-supply redundancy exists, but upstream shared failures remain. | [3.4](#34-explain-the-importance-of-resilience-and-recovery-in-security-architecture) |
| A secret is deleted from the current repository file. Is the exposure fixed? | Not necessarily. Rotate/revoke the secret, inspect history and distribution, and investigate possible misuse. | [2.4](#24-explain-types-of-vulnerabilities-and-attack-surfaces), [4.1](#41-given-a-scenario-apply-mitigating-controls-techniques-and-solutions-to-secure-the-environment) |
| A departed employee's account is disabled, but an issued application token remains active. What gap exists? | Incomplete deprovisioning. Account, sessions, tokens, delegated permissions, and associated access need appropriate revocation. | [4.5](#45-given-a-scenario-apply-concepts-related-to-identity-and-access-management) |
| A production machine may contain malware and volatile evidence. Should it always be powered off immediately? | No universal answer. Balance ongoing harm and preservation under the response plan; isolation and authorized memory collection may be appropriate. | [4.7](#47-summarize-concepts-associated-with-incident-response-activities), [4.8](#48-given-a-scenario-use-data-artifacts-and-sources-to-support-a-security-investigation) |
| A file's hash is recorded, but evidence handoffs are undocumented. Is chain of custody established? | No. Hashes help detect changes; custody requires handling/possession records. | [4.8](#48-given-a-scenario-use-data-artifacts-and-sources-to-support-a-security-investigation) |
| SLE is $40,000 and ARO is 0.2. What is ALE? | $8,000 per year as an estimated expected loss, not a guaranteed amount. | [5.2](#52-explain-the-impact-of-risk-management-processes-on-the-security-of-the-organization) |
| A vendor has an impressive audit report. Can all its services be assumed secure? | No. Check scope, period, exceptions, relevant services, and remediation; combine with continuing monitoring. | [5.3](#53-explain-the-assessment-and-management-processes-associated-with-third-party-risk), [5.5](#55-explain-concepts-associated-with-audit-and-assessment-activities) |
| A deletion request concerns records under a legal hold. What is the next step? | Coordinate with legal/privacy owners to determine applicable preservation and rights requirements; do not reflexively delete. | [5.4](#54-summarize-elements-of-effective-security-compliance) |
| Everyone completed phishing training, but suspicious messages are rarely reported. Is training effective? | Completion is an activity measure. Evaluate reporting, time to report, verification behavior, and repeat errors, then adjust training/processes. | [5.6](#56-given-a-scenario-apply-security-awareness-concepts-to-improve-organizational-security) |

### Final review routine

For every objective, explain its main terms without reading the table. Then invent an example and a counterexample. For scenarios, name the evidence, select a control, explain why it fits, and describe its limitation. Revisit any term you recognize but cannot apply. Practice comparing adjacent concepts, especially identity protocols, evidence types, recovery metrics, agreement types, and risk treatments.

## Sources and terminology notes

**Primary scope source:** The uploaded *CompTIA Security+ SY0-801 V8 Certification Exam Objectives, Version 2.0* (27 pages). Objective content is on pages 4–23; the 106-entry acronym list is on pages 24–26. Domain percentages here are taken from page 3 of that document. This guide follows the supplied PDF rather than substituting another exam version; it does not independently establish the document's publication status or exam availability.

**Supplemental primary references:**

- [NIST digital identity guidance](https://pages.nist.gov/800-63-4/sp800-63b.html): password and authenticator guidance discussed in 4.5.
- [OWASP prompt-injection prevention guidance](https://cheatsheetseries.owasp.org/cheatsheets/LLM_Prompt_Injection_Prevention_Cheat_Sheet.html): direct/indirect injection and layered controls discussed in 2.6.
- [MITRE ATT&CK resources](https://attack.mitre.org/resources/): tactics, techniques, and adversary behavior discussed in 5.5.
- [Lockheed Martin Cyber Kill Chain](https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html): attack-stage model discussed in 5.5.
- [European Data Protection Board — individual rights](https://www.edpb.europa.eu/sme/be-compliant/respect-individuals-rights_en): illustrative privacy rights and exceptions discussed in 5.4.

**Terminology notes:** The supplied acronym list uses “Portable Document Formats” and “Security Assertions Markup Language”; this guide uses the standard singular expansions. It uses both “Master Service Agreement” and “Master services agreement”; the glossary uses “Master Services Agreement.” “Data transpose,” “accounts” as an investigation stakeholder, and “functional/behavioral testing” are not defined in the PDF, so their explanations explicitly identify interpretation or context. Classification names are retained but not forced into a universal ranking. Broad items such as cryptographic tools, vulnerability types, and failure modes are explained with representative examples rather than attributed to a specific product.

[Return to index](#clickable-index)
