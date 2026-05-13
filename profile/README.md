# Sentinel Den

**Drop-in iOS security tooling for apps that can't afford to fail.**

Vendor-grade iOS security SDKs, binary-audit tooling, and engineering writing, by [Muhammad Khan](https://github.com/iamuhammadkhan) from Vancouver, British Columbia. Independent. No outside funding.

## What we ship

| Product | What it does | Status |
|---|---|---|
| **SentinelSDK** | Runtime defense: jailbreak / debugger / dylib-injection detection, integrity attestation, App Attest integration | [Available](https://sentinelden.com/sdk/sentinel) |
| **CryptoShield SDK** | Three-pin SPKI validation + payload encryption above TLS (ECDH + AES-256-GCM with replay-bound AAD) | [Available](https://sentinelden.com/sdk/cryptoshield) |
| **AgenticGuard SDK** | On-device LLM agent sandbox: typed tool registry, fail-closed intent verification, network egress policy, hash-chained audit trail | [Available](https://sentinelden.com/sdk/agenticguard) |
| **EnclaveVault SDK** | Typed Swift wrapper around the Apple Secure Enclave with CI-grade residency attestation | [Available](https://sentinelden.com/sdk/enclavevault) |
| **Sentinel Studio** | Notarized macOS app for auditing iOS binaries against OWASP MASVS rule packs. SARIF / PDF / Markdown report exports. | [Early access](https://sentinelden.com/studio) (free during beta) |

All five ship as code-signed `.xcframework` archives (or notarized macOS app, for Studio) with B2B licensing. The integration references at [sentinelden.com/docs](https://sentinelden.com/docs) cover the full API surface. Source for the commercial products is closed; the only public-source artifact under this org is below.

## Open source

📦 **[xcprivacy-lint](https://github.com/sentinelden/xcprivacy-lint)** — MIT-licensed Swift CLI that validates iOS `PrivacyInfo.xcprivacy` manifests against the API surface a binary actually touches. Catches missing and over-declared required-reason categories before App Store review does. Contributions welcome.

## Writing

The engineering blog at **[sentinelden.com/blog](https://sentinelden.com/blog)** covers the problems we built the SDKs to solve:

- Jailbreak detection beyond `sysctl`, layered Frida detection, Mach-O integrity
- TLS pinning under cert rotation, payload encryption above TLS, defeating MITM
- Secure Enclave residency, `biometryCurrentSet` vs `biometryAny`, App Attest cross-signing
- On-device LLM agent sandboxing, prompt injection in production, Apple Foundation Models tool-calling
- OWASP MASVS workflow on a real `.ipa`, macOS hardened-runtime entitlements for security tooling, SARIF for CI

Fifteen technical posts. No vendor fluff. RSS at [sentinelden.com/rss.xml](https://sentinelden.com/rss.xml).

## Reach us

- **Pre-sales · integration · licensing** → [sentinelden.com/contact](https://sentinelden.com/contact)
- **Coordinated security disclosure** → `security@sentinelden.com` (see [security policy](https://sentinelden.com/security))
- **General** → `mk@sentinelden.com`
- **Status** → [sentinelden.com/status](https://sentinelden.com/status)

## Where we ship from

Based in **Vancouver, British Columbia, Canada**. Contracts under BC law. EU and UK consumer-protection compliant. The website at **[sentinelden.com](https://sentinelden.com)** is the canonical surface for everything we publish; this org is for code and PR collaboration.

<p align="right"><sub>Not affiliated with, endorsed by, or specifically approved by Apple Inc. See <a href="https://sentinelden.com/trademarks">trademarks</a>.</sub></p>
