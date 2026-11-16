# kubebottle

> *Bottling stateful workspaces, GPU environments, and practical operators for Kubernetes.*

## Purpose

Kubernetes is built for ephemeral, stateless workloads — yet GPU development and interactive ML environments are inherently stateful. Developers install system packages, tweak dotfiles, and iterate inside containers whose writable layers are wiped on pod rescheduling, GPU scaling, or idle pause.

**kubebottle** builds focused, Kubernetes-native tools and operators that *bottle* — capture, version, and restore — stateful workspace environments without giving up declarative scheduling or standard cloud-native infrastructure.

## Projects

| Repository | Description |
| --- | --- |
| [**crema**](https://github.com/kubebottle/crema) | Declarative GPU Workspace Operator on Kubernetes — preserve container rootfs state across GPU scaling (`0 → 1 → 4`), pause & resume, and pod rescheduling. |
| [**artwork**](https://github.com/kubebottle/artwork) | Brand and mascot artwork for `kubebottle` and `crema` ([CC BY 4.0](https://github.com/kubebottle/artwork/blob/main/LICENSE)). |
| [**kube-webhook-certgen**](https://github.com/kubebottle/kube-webhook-certgen) | Forked utility for self-signed certificate generation in Kubernetes webhook setups. |

## Principles

- **Kubernetes-Native**: Standard CRDs, controllers, OCI registries, and kubelet/containerd workflows — no custom container runtime forks.
- **Clean State Separation**: Versioned rootfs snapshots in OCI images, persistent user data on PVCs.
- **Pragmatic Scope**: Small, well-documented tools aimed at real operational pain points in GPU and developer infrastructure.
