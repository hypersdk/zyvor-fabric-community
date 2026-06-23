---
> 🚀 **Trial v0.30.0 is live!** The latest release is available for trial today — [get started in 5 minutes →](#try-v030-in-5-minutes)

# Zyvor Fabric — Community

> **systemd-native private cloud control plane — 480+ REST endpoints, CLI, TUI, web UI, Terraform, K8s operator.**

![Version](https://img.shields.io/badge/version-v0.30.0-blue) ![Discussions](https://img.shields.io/github/discussions/hypersdk/zyvor-fabric-community) ![Issues](https://img.shields.io/github/issues/hypersdk/zyvor-fabric-community) ![License](https://img.shields.io/badge/license-Proprietary-red)

Public issue tracker and community feedback space for **Zyvor Fabric** by [Zyvor AI Labs](https://zyvor.dev).
The source code is maintained in a private repository. This repo is for bug reports, feature requests, UX feedback, and community discussion.

---

## What's new in v0.30

- vmspawn GA on Linux kernel 6.x — full systemd-machined integration with cgroup v2
- GPU passthrough wizard — guided UI workflow for VFIO passthrough setup, no manual IOMMU config
- Terraform provider v0.30 — manage VMs, networks, and storage pools as infrastructure code
- TUI v2 — redesigned vmctl-tui with 12 new views and live WebSocket metrics
- Clustering HA v0.30 — active/passive control plane with sub-30s failover

---

## Why Zyvor Fabric

| Problem | Zyvor Fabric answer |
|---------|--------------------|
| Private cloud means a heavy Proxmox or OpenStack stack | systemd-native VMs via vmspawn — runs on any modern Linux, no extra daemons |
| No unified API across CLI, web, and automation | 480+ REST endpoints, 3 WebSocket channels — every interface uses the same API |
| CLI or GUI is an either/or choice | CLI + TUI + Web + Terraform + K8s Operator — pick what fits the workflow |
| Enterprise needs RBAC and audit but hypervisors bolt them on | JWT, roles, audit export, encryption at rest — built into the daemon |
| GPU passthrough needs kernel expertise | First-class GPU API — passthrough wizard guides you through VFIO setup |

---

## Architecture

```
┌──────────────────────────────────────────────────────────────┐
│  Interfaces   vmctl CLI · vmctl-tui · Web UI · TF · Operator │
├──────────────────────────────────────────────────────────────┤
│  Daemon       Zyvor Fabric — 480+ REST endpoints · WebSocket │
├──────────────────────────────────────────────────────────────┤
│  Runtime      systemd-vmspawn · systemd-machined · KVM       │
└──────────────────────────────────────────────────────────────┘
```

---

## Try v0.30 in 5 minutes

```bash
# Build from source
git clone https://github.com/hypersdk/zyvor-fabric && cd zyvor-fabric
git checkout v0.30.0
make build && sudo make install

# Start the daemon
sudo systemctl enable --now zyvor-fabric

# CLI
vmctl vm list
vmctl vm create --name web-01 --cpus 2 --memory 4G --image ubuntu-22.04

# TUI
vmctl-tui

# Web UI → https://localhost:8443
```

**Requirements:** Linux (Ubuntu 22.04+ / Rocky Linux 9), KVM/QEMU, systemd 255+ (for vmspawn), Rust 1.78+ to build from source

---

## Report a bug

[Open a Bug Report →](../../issues/new?template=bug_report.yml)

Include: what you did, what happened, what you expected, your environment, screenshots or logs (redact secrets).

## Request a feature

[Open a Feature Request →](../../issues/new?template=feature_request.yml)

## UX feedback

[Open a UX Report →](../../issues/new?template=ux_feedback.yml)

## Ask a question

Use [GitHub Discussions](../../discussions) for open-ended questions, ideas, and roadmap conversations.

---

## Security

**Do not report security vulnerabilities publicly.**
Email **security@zyvor.dev** — see [SECURITY.md](SECURITY.md).

---

## Do not post

- Source code, internal configs, or architecture details
- API tokens, license keys, or credentials
- Private logs with sensitive data
- Security vulnerabilities — email security@zyvor.dev instead

---

## Join the community

⭐ [Star this repo](https://github.com/hypersdk/zyvor-fabric-community) · 💬 [Open a Discussion](https://github.com/hypersdk/zyvor-fabric-community/discussions) · 🐛 [Report a Bug](../../issues/new?template=bug_report.yml) · 📧 [hello@zyvor.dev](mailto:hello@zyvor.dev)

Maintained by [Zyvor AI Labs](https://zyvor.dev)
