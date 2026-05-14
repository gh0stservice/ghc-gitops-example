# 01 - Overview

This guide maps the gh0stportal onboarding surfaces to the files in this
repository.

## What gh0stcloud Owns

- tenant organization and member roles
- tenant limits and plan boundaries
- namespace and service-account scaffolding
- OpenBao namespace, auth roles, and secret paths
- Flux wiring from your GitOps repository
- billing and cost measurement

## What Your GitOps Repo Owns

- application manifests
- image versions
- application-level ingress objects
- PVC requests inside your tenant limits
- network policies inside policy bounds

Start with `kustomize/overlays/ghc-basic`, then compare the rendered manifests
with the Applications, Network, Data & Services, Observability, and Billing
pages in gh0stportal.
