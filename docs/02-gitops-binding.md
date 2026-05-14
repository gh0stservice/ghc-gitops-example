# 02 - GitOps Binding

The beginner path does not require GitOps input during registration. After your
trial tenant is active, gh0stportal can guide you through connecting a repo.

## Beginner

Use this repository as read-only reference material. Inspect the manifests and
learn the relationship between projects, namespaces, services, and ingress.

## Advanced

Fork this repository and connect the fork in gh0stportal:

- repository URL: your fork URL
- branch: `main`
- path: `kustomize/overlays/ghc-basic` or `kustomize/overlays/ghc-advanced`

After connecting, gh0stportal reports Flux source and kustomization state from
gh0stplane and gh0stoperator.

## Professional

Use the same binding model, but align repository layout, release branches,
namespace split, BYOD DNS, backup policy, and billing expectations before
production workloads are moved.
