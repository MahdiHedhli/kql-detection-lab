# kql-detection-lab

KQL-only threat hunting repo for Microsoft security telemetry.

No fluff. Just hunts, pivots, and ATT&CK tags.

## Coverage

- Entra ID hunts
- Defender hunts
- M365 hunts
- Incident triage pivots
- MITRE ATT&CK mapping

## Layout

- `identity/`: Entra sign-in and account takeover signal
- `exchange-online/`: inbox rules, forwarding, and mailbox change signal
- `service-principals/`: app and workload identity signal
- `privilege-escalation/`: role management and admin path signal
- `initial-access/`: phish, lure, and ingress signal
- `incident-triage/`: reusable alert expansion pivots

## Query Contract

Every `.kql` file should keep the same header:

- `Title`
- `Source tables`
- `ATT&CK`
- `Triage pivots`

Keep tunable variables at the top of each query. Keep comments short. Keep output analyst-friendly.

Queries in this repo assume Microsoft Sentinel / Log Analytics tables or Microsoft 365 Defender Advanced Hunting tables, as called out in each file.

[ATTACK-COVERAGE.md](ATTACK-COVERAGE.md) keeps the repo-level technique index tight.

## 🚧 Notes

These queries are intended for research, hunting, and detection engineering workflows. They should be tuned and validated within your environment to reduce noise and improve signal.

This repository reflects ongoing research into attacker behavior and defensive detection strategies in Microsoft cloud environments.

## 🧩 Related Work

- [ThreatPedia](https://threatpedia.wiki): Threat intelligence platform mapping attacker TTPs to detection logic and defensive strategies.
- [Identity Attack Paths](https://github.com/MahdiHedhli/identity-attack-paths): Detailed analysis of identity-based attack techniques (OAuth abuse, token theft, privilege escalation) with detection and mitigation guidance.
- [Cloud Threat Hunting Playbook](https://github.com/MahdiHedhli/cloud-threat-hunting-playbook): End-to-end investigation workflows for cloud and identity-focused incidents, aligned to real-world attacker behavior.
