# ATTACK-COVERAGE

| Query | ATT&CK |
| --- | --- |
| `identity/success-after-failures-same-ip.kql` | `T1110`, `T1078` |
| `identity/new-country-or-ip-success.kql` | `T1078` |
| `exchange-online/external-forwarding-inbox-rules.kql` | `T1114.003` |
| `exchange-online/mailbox-delegation-and-forwarding-changes.kql` | `T1098`, `T1114` |
| `service-principals/new-ip-or-resource-service-principal-signins.kql` | `T1078.004` |
| `service-principals/high-value-resource-service-principal-access.kql` | `T1078.004` |
| `privilege-escalation/after-hours-role-management-changes.kql` | `T1078`, `T1098` |
| `privilege-escalation/sensitive-role-assignments.kql` | `T1078`, `T1098` |
| `initial-access/phish-delivered-and-clicked.kql` | `T1566` |
| `initial-access/credential-lure-subject-spikes.kql` | `T1566.001`, `T1566.002` |
| `incident-triage/alert-entity-expansion.kql` | `triage pivot` |
| `incident-triage/user-device-mail-timeline-pivot.kql` | `triage pivot` |
