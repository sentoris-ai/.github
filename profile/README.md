# 📘 PROVENANCE Protocol

> **The Execution Provenance Layer for AI Agents**

[![PROVENANCE v1.0.0](https://img.shields.io/badge/PROVENANCE-v1.0.0-38BDF8?style=for-the-badge&logoColor=white)](https://provenance-protocol.dev)
[![Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue?style=for-the-badge&logoColor=white)](LICENSE)
[![Community Driven](https://img.shields.io/badge/Community-Driven-F472B6?style=for-the-badge&logoColor=white)](https://github.com/provenance-protocol/spec/discussions)

> 🔒 **"No server. No secret. No trust required."**
>
> PROVENANCE extends execution audit standards (IETF AAT, W3C PROV) with cryptographic verifiability — making every AI agent action **independently provable for the first time**.

---

## 🧭 The Agent Protocol Stack

PROVENANCE occupies the **Execution Provenance Layer** — the missing third pillar of the AI agent protocol stack:

```
┌─────────────────┐     ┌─────────────────┐
│ 🔗 MCP          │     │ 🤝 A2A          │
│ Tool Connectivity│     │ Agent Coordination│
└────────┬────────┘     └────────┬────────┘
         │                       │
         ▼                       ▼
    ┌───────────────────────────────┐
    │ 🤖 AI Agent                    │
    └────────┬───────────────────────┘
             │
             ▼
    ┌───────────────────────────────┐
    │ ✅ PROVENANCE                  │
    │ Execution Provenance Layer    │
    │ "Connect actions to proof"    │
    └───────────────────────────────┘
```

| Protocol | Layer | Responsibility |
|:---|:---|:---|
| **MCP** (Anthropic) | Tool Connectivity | Connect agents to tools |
| **A2A** (Google) | Agent Coordination | Connect agents to each other |
| **PROVENANCE** | **Execution Provenance** | **Connect actions to cryptographic proof** |

> MCP connects agents to tools. A2A connects agents to each other. PROVENANCE connects agent actions to cryptographic proof — without requiring trust in any infrastructure.

---

## 🎯 Why PROVENANCE?

| 🔐 Cryptographic Audit | 💰 Streaming Budget | 🛡️ Privacy Grading |
|:---|:---|:---|
| RFC 8785 JCS + SHA-256 | Atomic cost metering | `raw` / `masked` / `hash_only` |
| Tamper-evident, independently verifiable | Hard-stop at micro-cent precision | GDPR / CCPA compliant |

| 🔄 Deterministic Replay | 🔗 Zero-Trust Verification |
|:---|:---|
| Baseline-vs-candidate diff | Offline validation |
| Regression testing across model versions | No server. No secret. No trust. |

> 💡 **Key Insight**: Unlike audit logging standards that require trust in the infrastructure, PROVENANCE traces are **self-authenticating**. Anyone can verify execution integrity offline using only public algorithms and the raw trace JSON.

---

## 🗂️ Repository Map

| Repository | Description | Status |
|:---|:---|:---|
| [**spec**](https://github.com/provenance-protocol/spec) | Protocol specification & JSON Schemas (RFC 2119) | ✅ Stable v1.0.0 |
| [**prvn**](https://github.com/provenance-protocol/prvn) | Reference CLI — pronounced *"proven"* | 🚧 Beta |
| [**sdk-go**](https://github.com/provenance-protocol/sdk-go) | Go SDK | 🚧 Beta |
| [**sdk-python**](https://github.com/provenance-protocol/sdk-python) | Python SDK | 🚧 Beta |
| [**validator**](https://github.com/provenance-protocol/validator) | Independent trace verification | ✅ Stable |
| [**docs**](https://github.com/provenance-protocol/docs) | Guides, tutorials, examples | 📚 Active |

> 🗣️ **PRVN** is pronounced **/ˈpruːvən/** — "proven", as in "proven execution". It is the developer-facing engineering interface of the PROVENANCE Protocol.

---

## 🚀 Get Started in 60 Seconds

```bash
# Install the reference CLI
go install github.com/provenance-protocol/prvn/cmd/prvn@latest

# Initialize provenance tracking
prvn init --agent my-agent

# Verify a trace independently — no server required
prvn verify trace.json
```

📖 [Quick Start Guide](https://docs.provenance-protocol.dev/getting-started) · 📐 [Protocol Spec v1.0.0](https://spec.provenance-protocol.dev/v1.0.0) · 🧪 [Conformance Tests](https://github.com/provenance-protocol/spec/tree/main/conformance)

---

## 🏅 Certification Tiers

| Badge | Requirements | Use Case |
|:---|:---|:---|
| 🔵 **Core Compatible** | Schema + Proof + Headers | Lightweight SDKs, embedded agents |
| 🟢 **Full Compatible** | Core + Budget + State Machine + Privacy | Production proxies, enterprise gateways |
| 🟡 **Extended Compatible** | Full + ≥2 official extension namespaces | Compliance-critical deployments |

[View Certified Implementations →](https://github.com/provenance-protocol/spec/blob/main/ADOPTERS.md)

---

## 🌐 Standards Alignment

PROVENANCE is not a replacement for existing standards — it extends them with cryptographic provability:

| Standard | PROVENANCE's Role |
|:---|:---|
| **W3C PROV** | Extended for the agent execution domain (cf. PROV-AGENT) |
| **IETF AAT** | Complementary — AAT defines log *format*, PROVENANCE adds *provability* |
| **NIST AI RMF 1.0** | Capabilities map to Govern / Map / Measure / Manage pillars |
| **OpenTelemetry** | Exports traces as OTel spans with `gen_ai.*` semantic conventions |

---

## 🤝 Ecosystem Integration

### OpenClaw
PROVENANCE captures every skill installation and tool call as cryptographically signed provenance data. In an ecosystem where malicious plugins can slip past static analysis, PROVENANCE ensures that **all actions — benign or malicious — are indelibly recorded and verifiable**.

### Hermes Agent
Hermes advocates for trustworthy, controllable, auditable agents across the full autonomous lifecycle. PROVENANCE provides the cryptographic foundation for **runtime verifiability** — proving that agent behaviors align with declared policies throughout autonomous evolution.

### OpenTelemetry
PROVENANCE traces export seamlessly into existing observability stacks via OTel `gen_ai.*` semantic conventions — **observability without trust is just monitoring; with PROVENANCE, it becomes verifiability**.

---

## ⚖️ Key Tradeoffs

Great protocols are honest about what they optimize for:

| Tradeoff | PROVENANCE's Stance |
|:---|:---|
| **Real-time vs. eventual verifiability** | Guarantees eventual cryptographic verifiability; real-time checks are configurable |
| **Trace completeness vs. agent performance** | Trace depth is configurable, guided by minimal-overhead policy at runtime |
| **Standard compliance vs. innovation speed** | Aligns with W3C PROV and IETF AAT, extending them with cryptographic integrity |

---

## 🤲 Join the Community

PROVENANCE is built in the open, governed by a [community TSC](https://github.com/provenance-protocol/spec/blob/main/GOVERNANCE.md), and guided by an [RFC process](https://github.com/provenance-protocol/spec/blob/main/GOVERNANCE.md#3-rfc-request-for-comments-process).

[💬 Discussions](https://github.com/provenance-protocol/spec/discussions) · [📜 RFC Proposals](https://github.com/provenance-protocol/spec/issues?q=label%3Arfc) · [🐛 Report Issue](https://github.com/provenance-protocol/spec/issues) · [🔐 Security Policy](https://github.com/provenance-protocol/spec/blob/main/SECURITY.md) · [📖 Contributing Guide](https://github.com/provenance-protocol/spec/blob/main/CONTRIBUTING.md)

> *"Trust is not enough. You need proof."*

---

<div align="center" style="color: #64748b; font-size: 0.9em; margin-top: 2em;">

PROVENANCE™ is a community-driven open standard.  
The PROVENANCE name and logo are marks of the PROVENANCE Protocol community.  
PRVN is the reference implementation.  
Not affiliated with any single company or vendor.

[Apache License 2.0](LICENSE) · [Code of Conduct](CODE_OF_CONDUCT.md)

</div>
