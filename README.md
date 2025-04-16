# FluxCD GitOps – Talos Cluster Config

This repository holds the GitOps configuration for the `dev-cluster` running on Talos Linux.

## Structure

- `clusters/dev-cluster` – Cluster-specific configs and apps
- Apps managed via Flux:
  - `ingress-nginx`
  - `cert-manager`
  - `external-dns`

## How to Bootstrap

```bash
flux bootstrap github \
  --owner=<your-user> \
  --repository=flux-talos-config \
  --path=clusters/dev-cluster \
  --personal
```

Ensure Talos cluster is already bootstrapped and FluxCD is running.
