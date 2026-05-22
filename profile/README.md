# Sentinel Den

**Drop-in iOS security tooling for apps that can't afford to fail.**

Vendor-grade iOS security SDKs, binary-audit tooling, and engineering writing, by [Muhammad Khan](https://github.com/iamuhammadkhan) from Vancouver, British Columbia. Independent. No outside funding.

## What we ship

### Runtime defense

| Product | What it does |
|---|---|
| **[RuntimeGuard SDK](https://sentinelden.com/sdk/runtimeguard)** | Jailbreak / debugger / dylib-injection detection, integrity attestation, App Attest cross-signing, risk-scored security reports |
| **[BehaviorGuard SDK](https://sentinelden.com/sdk/behaviorguard)** | Continuous behavioral biometrics - touch dynamics, motion patterns, keyboard rhythm - with on-device baseline learning |
| **[PresenceKit SDK](https://sentinelden.com/sdk/presencekit)** | NPU-pinned continuous presence verification: liveness, gaze, face-region pinning beyond FaceID |

### Data & transport

| Product | What it does |
|---|---|
| **[PayloadGuard SDK](https://sentinelden.com/sdk/payloadguard)** | Three-pin SPKI TLS validation plus ECDH + AES-256-GCM payload encryption above TLS, with replay-bound AAD |
| **[EnclaveVault SDK](https://sentinelden.com/sdk/enclavevault)** | Typed Swift wrapper around the Apple Secure Enclave with CI-grade residency attestation |
| **[RedactKit SDK](https://sentinelden.com/sdk/redactkit)** | On-device PII redaction across visual, audio, and text - faces, plates, document edges, speech PII, structured text |

### Surface protection

| Product | What it does |
|---|---|
| **[ScreenGuard SDK](https://sentinelden.com/sdk/screenguard)** | Capture protection, forensic HMAC watermarks, ReplayKit-bypass defenses |
| **[InputGuard SDK](https://sentinelden.com/sdk/inputguard)** | Secure keyboard + clipboard isolation, paste-source attestation |

### AI & agents

| Product | What it does |
|---|---|
| **[AgenticGuard SDK](https://sentinelden.com/sdk/agenticguard)** | On-device LLM agent sandbox: typed tool registry, fail-closed intent verification, egress policy, hash-chained audit trail |
| **[IntentKit SDK](https://sentinelden.com/sdk/intentkit)** | Offline SLM intent engine: natural language → structured tool calls, no cloud, Ed25519-signed model artifacts |
| **[AnomalyKit SDK](https://sentinelden.com/sdk/anomalykit)** | On-device anomaly detection across telemetry, sensors, acoustics, and behavior with INT4-quantized models |

### Audit & compliance

| Product | What it does |
|---|---|
| **[ManifestGuard SDK](https://sentinelden.com/sdk/manifestguard)** | Debug-only privacy-manifest auditor: catches missing and over-declared required-reason categories before App Store review does |
| **[SentinelDen Studio](https://sentinelden.com/audit)** | Notarized macOS app for auditing iOS binaries against OWASP MASVS rule packs. SARIF / PDF / Markdown report exports. Linux `sentinelctl` CLI variant included. |

All twelve SDKs ship as code-signed `.xcframework` archives (or as a notarized macOS app for SentinelDen Studio) with B2B licensing. The integration references at [sentinelden.com/docs](https://sentinelden.com/docs) cover the full API surface. Source for the commercial products is closed; the only public-source artifact under this org is below.

## Open source

**[xcprivacy-lint](https://github.com/sentinelden/xcprivacy-lint)**, MIT-licensed Swift CLI that validates iOS `PrivacyInfo.xcprivacy` manifests against the API surface a binary actually touches. Catches missing and over-declared required-reason categories before App Store review does. Contributions welcome.

## Writing

The engineering blog at **[sentinelden.com/blog](https://sentinelden.com/blog)** covers the problems we built the SDKs to solve:

- Jailbreak detection beyond `sysctl`, layered Frida detection, Mach-O integrity
- TLS pinning under cert rotation, payload encryption above TLS, defeating MITM
- Secure Enclave residency, `biometryCurrentSet` vs `biometryAny`, App Attest cross-signing
- On-device LLM agent sandboxing, prompt injection in production, Apple Foundation Models tool-calling
- Offline SLM intent extraction, INT4 quantization budgets on iPhone 17 Pro, MLX vs Core ML backend selection
- Continuous behavioral biometrics, NPU-pinned liveness, behavioral signals beyond FaceID
- On-device PII redaction across visual / audio / text on a single policy surface
- Sensor and acoustic anomaly detection, Bayesian fusion across modalities
- OWASP MASVS workflow on a real `.ipa`, macOS hardened-runtime entitlements for security tooling, SARIF for CI

Ninety-plus technical posts. No vendor fluff. RSS at [sentinelden.com/rss.xml](https://sentinelden.com/rss.xml).

## Reach us

- **Pre-sales · integration · licensing** → [sentinelden.com/contact](https://sentinelden.com/contact)
- **Coordinated security disclosure** → `security@sentinelden.com` (see [security policy](https://sentinelden.com/security))
- **General** → `mk@sentinelden.com`
- **Status** → [sentinelden.com/status](https://sentinelden.com/status)

## Where we ship from

Based in **Vancouver, British Columbia, Canada**. Contracts under BC law. EU and UK consumer-protection compliant. The website at **[sentinelden.com](https://sentinelden.com)** is the canonical surface for everything we publish; this org is for code and PR collaboration.

<p align="right"><sub>Not affiliated with, endorsed by, or specifically approved by Apple Inc. See <a href="https://sentinelden.com/trademarks">trademarks</a>.</sub></p>
