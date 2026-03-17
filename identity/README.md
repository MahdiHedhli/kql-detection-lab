# identity

Entra ID hunts keyed to sign-in abuse and account takeover.

- `success-after-failures-same-ip.kql`: repeated sign-in failures followed by success from the same IP. ATT&CK: `T1110`, `T1078`
- `new-country-or-ip-success.kql`: successful sign-ins from new countries or unseen IPs per user. ATT&CK: `T1078`
