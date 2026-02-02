# ⭐ Polaris - Homelab Infrastructure

> *Your North Star in the Infrastructure Galaxy*

Complete homelab infrastructure managed as code using Talos OS Kubernetes cluster and FluxCD GitOps practices.

## 🎯 Overview

Polaris is a production-grade homelab environment designed for learning, experimentation, and hosting self-hosted applications. Built on modern cloud-native technologies, it serves as both a personal development platform and a portfolio showcase.

### Philosophy

- **Infrastructure as Code**: Everything is versioned and declarative
- **GitOps-driven**: Git is the single source of truth
- **Immutable Infrastructure**: Talos OS for secure, minimal Kubernetes nodes
- **Observable**: Comprehensive monitoring and logging stack
- **Scalable**: Designed to grow from single node to multi-node cluster

### Infrastructure Stack
```
┌────────────────────────────────────────────────────────┐
│                   Polaris Homelab                      │
├────────────────────────────────────────────────────────┤
│                                                        │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐  │
│  │  polaris-m01 │  │  polaris-m02 │  │  polaris-m03 │  │
│  │   (Master)   │  │   (Master)   │  │   (Master)   │  │
│  │   Talos OS   │  │   Talos OS   │  │   Talos OS   │  │
│  └──────────────┘  └──────────────┘  └──────────────┘  │
│                                                        │
│  ┌──────────────────────────────────────────────────┐  │
│  │         Kubernetes Cluster (v1.35.0)             │  │
│  └──────────────────────────────────────────────────┘  │
│                                                        │
│  ┌──────────────────────────────────────────────────┐  │
│  │  FluxCD GitOps Engine                            │  │
│  │  ├─ Source Controller                            │  │
│  │  ├─ Kustomize Controller                         │  │
│  │  ├─ Helm Controller                              │  │
│  │  └─ Notification Controller                      │  │
│  └──────────────────────────────────────────────────┘  │
│                                                        │
└────────────────────────────────────────────────────────┘
```

### Technology Stack

| Component | Technology | Purpose |
|-----------|-----------|---------|
| **OS** | Talos OS | Immutable, secure Kubernetes-focused OS |
| **Orchestration** | Kubernetes | Container orchestration |
| **GitOps** | FluxCD | Continuous deployment from Git |
| **Networking** | Cilium | CNI (Container Network Interface) |
| **Ingress** | Traefik | HTTP(S) routing and load balancing |
| **Storage** | Longhorn | Persistent volume management |
| **Certificates** | cert-manager | Automated TLS certificate management |
| **Monitoring** | Prometheus + Grafana | Metrics collection and visualization |
| **Logging** | Loki + Promtail | Log aggregation and querying |
| **Secrets** | SOPS | Encrypted secrets in Git |

## 🎯 Roadmap

- [x] Basic Kubernetes cluster with Talos OS
- [x] FluxCD GitOps setup
- [ ] SOPS Secrets
- [ ] Install core component (MetalLB, Longhorn, cert-manager, Traefik)
- [ ] Configure Renovate
- [ ] Monitoring stack (Prometheus + Grafana)
- [ ] High availability setup (3 master nodes)
- [ ] Migrate to External secrets operator integration
- [ ] Automated backup to cloud storage

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🌟 Acknowledgments

- [Talos OS](https://www.talos.dev/) - Immutable Kubernetes OS
- [FluxCD](https://fluxcd.io/) - GitOps toolkit
- [home-ops](https://github.com/onedr0p/home-ops) - Inspiration
- The Homelab community on r/homelab

---

**Polaris Homelab** - *Where Infrastructure Meets Innovation* ⭐

Last updated: 2026-02-02
