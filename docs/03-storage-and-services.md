# 03 - Storage and Services

The advanced overlay includes a small `PersistentVolumeClaim` named
`ghc-example-app-data`.

Use it to learn how storage requests appear in gh0stportal:

- Data & Services shows storage and managed-service intent.
- Billing shows storage cost allocation once runtime measurement is available.
- Tenant limits and policy bounds decide what can be created.

Do not store secrets in PVCs or manifests. Use OpenBao-backed workflows shown
in gh0stportal for service credentials.
