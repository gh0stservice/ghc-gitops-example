# 04 - Network and Ingress

The base example contains a standard Kubernetes `Ingress` and the advanced
overlay adds a `NetworkPolicy`.

## Default Ingress

Use the default gh0stcloud ingress path for early trials. Replace the placeholder
host with a hostname assigned to your tenant before applying the overlay.

## BYOD Ingress

Bring-your-own-domain onboarding belongs in gh0stportal Network & Exposure.
That page reports the required DNS record and verification state. Add BYOD
hostnames to GitOps only after the DNS handoff is ready.

## Network Policy

The advanced policy is intentionally simple. It demonstrates ingress and DNS
egress structure without modelling every production dependency.
