# ghc-gitops-example

Example GitOps repository for gh0stcloud onboarding.

This repository is intentionally small. It gives new gh0stcloud tenants a safe
reference for the first application, while advanced users can fork it and wire
their own repository through the gh0stportal onboarding flow.

## Onboarding Paths

| Path | Use when | What to do |
| --- | --- | --- |
| Beginner | You want to explore gh0stcloud before wiring your own GitOps repo. | Read the guided docs and inspect `kustomize/overlays/ghc-basic`. |
| Advanced | You already have a repo and want to connect it to Flux. | Fork this repo, edit placeholders, and connect the fork in gh0stportal. |
| Professional | You are planning production migration or multi-environment rollout. | Use this repo as a vocabulary baseline, then coordinate policy, DNS, data, and billing decisions before launch. |

## Directory Layout

```text
kustomize/
  base/generic/            shared app resources
  overlays/ghc-basic/      smallest beginner example
  overlays/ghc-advanced/   adds PVC and NetworkPolicy examples
  overlays/ghc-professional/ reserved production-readiness scaffold
docs/
  01-overview.md
  02-gitops-binding.md
  03-storage-and-services.md
  04-network-and-ingress.md
  05-billing-and-costs.md
```

## How To Use

1. Start with the gh0stportal onboarding page.
2. Choose the onboarding path that fits your experience level.
3. For beginner exploration, open the docs in this repo and compare them with
   the portal workspaces.
4. For advanced GitOps, fork this repo and replace:
   - `ghc-nsp-replace-me-app`
   - `example.replace-me.dev.gh0stcloud.de`
   - image, host, and resource values that belong to your application.
5. Connect your fork in gh0stportal under Applications and GitOps Bindings.

## Validation

Run these commands before connecting a fork:

```bash
kustomize build kustomize/overlays/ghc-basic
kustomize build kustomize/overlays/ghc-advanced
kustomize build kustomize/overlays/ghc-professional
```

## Safety Boundaries

- Do not commit secrets to this repo.
- Use OpenBao and gh0stportal service-account guidance for credentials.
- Keep BYOD DNS records and production hostnames out of examples until they are
  assigned to your tenant.
- Treat this repo as educational source, not as a production SLA template.
