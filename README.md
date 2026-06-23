# Zyvor fabric — Community

> **systemd-native private cloud control plane — 480+ REST endpoints, CLI, TUI, web, Terraform, Kubernetes operator**

Public issue tracker and community feedback space for **Zyvor-fabric** by [Zyvor AI Labs](https://zyvor.dev).

The source code is maintained in a private repository. This repo is for:
- Bug reports
- Feature requests
- UX feedback
- Documentation gaps
- Questions and discussion

---

## Key features

- systemd-native VMs via vmspawn — no heavyweight hypervisor stack
- 480+ REST endpoints, 3 WebSocket channels
- 5 interfaces: CLI (vmctl), TUI, Web UI (37+ pages), Kubernetes Operator, Terraform provider
- RBAC, JWT auth, audit log export, encryption at rest
- GPU passthrough — first-class GPU API on Linux KVM
- Clustering, HA, storage, networking built-in
- 40 Rust crates, ~87K LOC

---

## Installation

**Build and install:**
```bash
git clone https://github.com/hypersdk/zyvor-fabric && cd zyvor-fabric
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

**Requirements:** Linux (Ubuntu 22.04+ / Rocky 9), KVM/QEMU, systemd 255+ (for vmspawn), Rust 1.78+ to build from source

---

## Report a bug

[Open a Bug Report →](../../issues/new?template=bug_report.yml)

Include: what you did, what happened, what you expected, your environment, and screenshots/logs (redact secrets).

## Request a feature

[Open a Feature Request →](../../issues/new?template=feature_request.yml)

## UX feedback

[Open a UX Feedback →](../../issues/new?template=ux_feedback.yml)

## Ask a question

Use [GitHub Discussions](../../discussions) for open-ended questions, ideas, and roadmap conversations.

---

## Security

**Do not report security vulnerabilities publicly.**

Email **security@zyvor.dev** — see [SECURITY.md](SECURITY.md).

---

## Do not post

- Source code or internal configuration
- API tokens, license keys, or credentials  
- Private logs with sensitive data
- Security vulnerabilities (email security@zyvor.dev)

---

Maintained by [Zyvor AI Labs](https://zyvor.dev)
