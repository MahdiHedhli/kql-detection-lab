# privilege-escalation

Entra and admin-path hunts for role abuse and privilege change signal.

- `after-hours-role-management-changes.kql`: role management changes outside normal working hours. ATT&CK: `T1078`, `T1098`
- `sensitive-role-assignments.kql`: assignments or activations involving high-impact roles. ATT&CK: `T1078`, `T1098`
