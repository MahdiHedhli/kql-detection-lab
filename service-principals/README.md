# service-principals

Workload identity hunts for service principal drift and high-value access.

- `new-ip-or-resource-service-principal-signins.kql`: first-seen IP or target resource for a service principal. ATT&CK: `T1078.004`
- `high-value-resource-service-principal-access.kql`: service principals touching sensitive Microsoft cloud resources. ATT&CK: `T1078.004`
