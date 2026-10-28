# Compromised Windows Analysis — Forensic Computing Lab

## Overview

**Status: In progress — investigation and lab completion are not yet documented.**

This Forensic Computing lab uses TryHackMe’s Compromised Windows Analysis room to practice investigating a compromised Windows workstation. This write-up is a working template for recording evidence, testing explanations, and reconstructing an incident timeline. No host findings, indicators of compromise, or completion claims have been established here.

- **Student:** Hien Long (Jayden) Nguyen
- **Portfolio entry updated:** October 28, 2026
- **Investigation date:** Pending
- **Room:** [TryHackMe: Compromised Windows Analysis](https://tryhackme.com/room/compromisedwindowsanalysis)

## Tools and Topics

Planned tools and topics from the lab materials and room; their use is not yet documented:

- **Event Viewer:** Filter, search, and export Windows event logs.
- **Task Scheduler:** Inspect task definitions, triggers, actions, and account context for persistence.
- **LECmd and PECmd:** Parse LNK and Prefetch artifacts for file-access and execution evidence.
- **AmcacheParser:** Review application metadata, paths, and hashes alongside other evidence.
- **Timeline Explorer:** Review parsed CSV records and correlate timestamps.
- **Forensic analysis:** Root cause, intrusion, defense evasion, execution, persistence, and event sequencing.

## Workflow

- [x] Review the provided assignment and Windows event-log guidance.
- [x] Prepare this in-progress portfolio entry and evidence templates.
- [ ] Start the authorized lab environment and record host details and time settings.
- [ ] Preserve relevant artifacts and export event logs before analysis.
- [ ] Investigate scheduled tasks and related persistence evidence.
- [ ] Correlate recently accessed files, execution artifacts, and application metadata.
- [ ] Analyze logs for remote access and security configuration changes.
- [ ] Build an evidence-backed timeline and assess the likely root cause.
- [ ] Complete the room, capture dated completion evidence, and write the reflection.

## Evidence Handling and Environment

Record the actual lab environment before filling in findings. Retain original exports and analyze working copies. Record collection actions that could change the live lab system.

| Field | Value |
| --- | --- |
| Hostname and Windows version | Pending |
| Relevant user accounts | Pending |
| Collection date and examiner | Pending |
| Host time zone and UTC offset | Pending |
| Clock differences or synchronization concerns | Pending |
| Tool names, versions, commands, and filters | Pending |

For each artifact, record its source, collection time, SHA-256 hash, and the working copy or export used. Save screenshots and analysis exports only after reviewing them for sensitive information. The provided teaching documents are reference materials, not acquired host evidence.

| Evidence ID | Source path or log channel | Collected at, with zone | SHA-256 | Working copy or export | Notes |
| --- | --- | --- | --- | --- | --- |
| Pending | Pending | Pending | Pending | Pending | No host evidence recorded |

## Windows Forensic Artifacts

The following are investigation targets, not observed findings. Confirm paths and availability on the lab host.

| Artifact | Planned examination | Interpretation limits |
| --- | --- | --- |
| Scheduled tasks and `C:\Windows\System32\Tasks` | Task name, creation time, trigger interval, action, arguments, principal, and referenced files | A task definition alone does not prove successful execution or malicious intent |
| Recent LNK files in the relevant user profile | Target path, source and target timestamps, and references to archives or files | Distinguish shortcut timestamps from target timestamps; a reference alone does not prove execution |
| `C:\Windows\Prefetch` | Executable name, run count, recorded run times, and related paths using PECmd | Correlate execution traces with logs; absence is not proof of non-execution |
| `C:\Windows\appcompat\Programs\Amcache.hve` or supplied parsed export | File metadata, full path, hash, and timestamp fields | Amcache metadata alone does not establish execution or an exact execution time |
| Windows event logs | Remote access, security changes, process or task activity where available | Interpret each event with its provider, channel, fields, and audit coverage |

### Artifact Findings Template

Repeat for each item investigated:

- **Question or hypothesis:** Pending
- **Evidence ID and exact record or file:** Pending
- **Tool, version, command, and filter:** Pending
- **Observed values and timestamps, with zone:** Pending
- **Interpretation:** Pending
- **Corroborating evidence:** Pending
- **Alternative explanations and limitations:** Pending
- **Screenshot or export reference:** Pending

## Windows Event Log Analysis

Use the provided guidance to open Event Viewer (`eventvwr.msc`), filter by time, provider, and event ID, search relevant terms, and save logs with **Save All Events As…**. Preserve the original EVTX alongside any filtered CSV or screenshot. An event ID must be interpreted in the context of its provider and channel.

Planned review includes Security, System, and Application logs where relevant, plus the room’s TerminalServices-RemoteConnectionManager and Windows Defender Operational channels. Correlate remote-access records with session and logon evidence where available; an isolated authentication event does not establish the full intrusion sequence. Separate Defender changes from firewall changes and record only the control actually supported by evidence.

| Evidence ID | Provider and channel | Event ID / record ID | Raw timestamp and zone | Account / source address | Observed event details | Interpretation and corroboration |
| --- | --- | --- | --- | --- | --- | --- |
| Pending | Pending | Pending | Pending | Pending | No log records analyzed here | Pending |

## Persistence and Execution Evidence

Document any suspected persistence mechanism’s exact task or configuration name, action, arguments, interval, account, and referenced executable. Then seek independent evidence that the action ran. A recurring trigger or suspicious command is a lead until supported by records.

| Question | Evidence to record | Current result |
| --- | --- | --- |
| What maintained persistence? | Task definition, timestamps, trigger, action, account, and related logs | Pending |
| What file was executed? | Full path, hash and algorithm, Prefetch details, and available process records | Pending |
| When and how often did execution occur? | Recorded run times and count, with corroborating records | Pending |
| What network activity followed? | Available connection records, destination, port, process linkage, and time | Pending |

## Root Cause Analysis

Test the room’s suggested attack path against collected evidence. Treat scenario descriptions and walkthrough examples as context, not personal findings. Do not infer the initial access method, archive contents, payload behavior, or deletion solely from a filename or one artifact.

- **Likely initial access and supporting records:** Pending
- **File arrival, access, and execution sequence:** Pending
- **Security configuration changes and supporting records:** Pending
- **Persistence and relationship to the suspected executable:** Pending
- **Alternative explanations and missing evidence:** Pending
- **Root-cause conclusion and confidence:** Pending; no conclusion established

## Timeline

Preserve raw timestamps and their source fields. Record the host time zone and normalize to UTC only after verifying the offset applicable to each event. Distinguish file creation, modification, access, log event time, and parser-derived values. Rows below are prompts, not a confirmed order of events.

| Activity to investigate | Raw timestamp / field / zone | Normalized UTC | Evidence ID and record | Interpretation / confidence |
| --- | --- | --- | --- | --- |
| Remote access or session activity | Pending | Pending | Pending | Unverified |
| Security configuration change | Pending | Pending | Pending | Unverified |
| Archive or payload arrival and access | Pending | Pending | Pending | Unverified |
| Suspected executable run | Pending | Pending | Pending | Unverified |
| Persistence creation and subsequent activity | Pending | Pending | Pending | Unverified |
| Possible cleanup or deletion, if supported | Pending | Pending | Pending | Unverified |

## Results

**Pending.** The assignment and guidance have been reviewed and the investigation template prepared. No acquired host artifacts, analyzed log records, verified indicators, attack timeline, or room completion screenshots are included yet.

## Reflection and Submission Checklist

After completing the investigation, write one short paragraph, within the assignment’s one-page maximum, covering new skills or concepts, how the artifacts help reconstruct an attack path, and how the knowledge improves understanding of Windows privacy and security. **Reflection: Pending.**

- [ ] Prepare the required formatted Word or PDF submission with student name, date, and lab title.
- [ ] Add a screenshot of the entire room completed, or screenshots showing completion of all tasks.
- [ ] Ensure the device date and time are visible in the completion screenshots.
- [ ] Link reviewed evidence and screenshots from this write-up, replace pending fields with supported observations, and update status only after completion is documented.

## Materials

- [TryHackMe room](https://tryhackme.com/room/compromisedwindowsanalysis)
- [Provided Forensic Computing lab assignment](./documents/Forensics%20Lab_Compromised%20Windows%20Analysis.pdf)
- [Provided Windows logs investigation guidance](./documents/Guidance%20-%20Windows%20Logs%20Investigation.docx)
- [Back to portfolio](../../README.md)
