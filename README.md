# KQL Detection Lab

![Status](https://img.shields.io/badge/status-active%20research-0b7285)
![Focus](https://img.shields.io/badge/focus-Entra%20ID%20%7C%20Defender%20%7C%20M365-1d3557)
![Coverage](https://img.shields.io/badge/coverage-12%20queries%20%7C%206%20packs-6c584c)
![Maintained](https://img.shields.io/badge/updated-2026--03--17-588157)

> Pure signal. No fluff. Just hunts, pivots, and ATT&CK tags for Microsoft cloud telemetry.

A practical collection of threat hunting queries, detection logic, and investigation pivots built using Kusto Query Language (KQL) across Microsoft security platforms.

This repository focuses on real-world attacker behaviors observed in enterprise environments, with an emphasis on identity-based attacks, cloud telemetry, and SIEM-driven detection engineering.

## 🔍 What This Repo Covers

- Threat hunting queries for Microsoft Sentinel
- Detection logic for Entra ID identity events
- Investigation pivots across Microsoft 365 and cloud logs
- Behavioral detections aligned to MITRE ATT&CK
- High-signal queries for incident triage and escalation

## 🚀 Quick Start

| If you are hunting for... | Start here |
| --- | --- |
| Suspicious sign-in patterns and account takeover signal | [identity/](identity/README.md) |
| Inbox rules, forwarding, and mailbox persistence | [exchange-online/](exchange-online/README.md) |
| Service principal, app, and workload identity abuse | [service-principals/](service-principals/README.md) |
| Role assignments and admin-path privilege changes | [privilege-escalation/](privilege-escalation/README.md) |
| Initial access, phishing, and lure-driven signal | [initial-access/](initial-access/README.md) |
| Alert expansion and cross-telemetry pivots | [incident-triage/](incident-triage/README.md) |
| ATT&CK technique coverage across the repo | [ATTACK-COVERAGE.md](ATTACK-COVERAGE.md) |

## 🧠 Focus Areas

- Identity-based attacks, including privilege escalation and token-focused abuse paths
- Suspicious sign-in patterns and authentication anomalies
- Service principal and application abuse
- Persistence techniques in Microsoft cloud environments
- High-signal pivots for triage across identity, device, and mail telemetry

## ⚙️ Structure

| Path | What it contains |
| --- | --- |
| `identity/` | Entra ID and authentication-focused detections |
| `service-principals/` | Application, workload identity, and app abuse scenarios |
| `exchange-online/` | Mailbox rules, forwarding, and phishing persistence signal |
| `privilege-escalation/` | Role assignments, admin activity, and escalation paths |
| `initial-access/` | Suspicious access patterns, lure activity, and ingress signal |
| `incident-triage/` | Reusable alert expansion and analyst pivot queries |
| `ATTACK-COVERAGE.md` | Repo-level ATT&CK technique index |

## 🎯 Goal

To bridge the gap between threat intelligence and actionable detection logic, enabling defenders to identify and respond to attacker activity using native Microsoft telemetry.

## 📐 Query Contract

Every `.kql` file in this repo should keep the same header:

- `Title`
- `Source tables`
- `ATT&CK`
- `Triage pivots`

Keep tunable variables at the top of each query. Keep comments short. Keep output analyst-friendly.

Queries in this repo assume Microsoft Sentinel / Log Analytics tables or Microsoft 365 Defender Advanced Hunting tables, as called out in each file.

## 🚧 Notes

These queries are intended for research, hunting, and detection engineering workflows. They should be tuned and validated within your environment to reduce noise and improve signal.

This repository reflects ongoing research into attacker behavior and defensive detection strategies in Microsoft cloud environments.

## 🧩 Related Work

- [ThreatPedia](https://threatpedia.wiki): Threat intelligence platform mapping attacker TTPs to detection logic and defensive strategies.
- [Identity Attack Paths](https://github.com/MahdiHedhli/identity-attack-paths): Detailed analysis of identity-based attack techniques, including OAuth abuse, token theft, privilege escalation, and detection guidance.
- [Cloud Threat Hunting Playbook](https://github.com/MahdiHedhli/cloud-threat-hunting-playbook): End-to-end investigation workflows for cloud and identity-focused incidents, aligned to real-world attacker behavior.
