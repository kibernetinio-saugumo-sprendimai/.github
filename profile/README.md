<div align="center">
  <img src="https://raw.githubusercontent.com/kibernetinio-saugumo-sprendimai/.github/main/assets/logo/safestack.png" width="112" alt="SafeStack logo">
  <h1>SafeStack</h1>
  <p><strong>Verifiable security systems for teams that cannot afford silent failure.</strong></p>
  <p>
    <a href="https://safestack.engineering">Official Showcase</a> ·
    <a href="https://github.com/kibernetinio-saugumo-sprendimai/safestack-repo-map">Repository Map</a> ·
    <a href="https://github.com/kibernetinio-saugumo-sprendimai/safestack-project-public-keys">Public Key Registry</a> ·
    <a href="https://github.com/kibernetinio-saugumo-sprendimai/safestack-validation-registry">Validation Registry</a> ·
    <a href="https://github.com/kibernetinio-saugumo-sprendimai/Verification-artifacts">Verification Artifacts</a> ·
    <a href="https://github.com/kibernetinio-saugumo-sprendimai/.github/blob/main/SECURITY.md">Security Policy</a>
  </p>
</div>

---

SafeStack builds security infrastructure around a strict standard: critical actions must be bounded, attributable, isolated by default, and independently verifiable. We engineer deterministic security controls across zero-trust policy engines, audit automation, host telemetry daemons, and cryptographic canons.

## Operating Model & Key Isolation

```mermaid
flowchart LR
    A[Offline Root Key] -->|signs| B[Public Project Registry]
    B --> C[Project 001
Audit System]
    B --> D[Project 010
Sentinel]
    B --> E[Project 014
Zero Trust]
    C --> F[Signed Artifacts]
    D --> G[Verified Telemetry]
    E --> H[Policy Decisions]
    F --> I{Independent Verification}
    G --> I
    H --> I
    I -->|valid| J[Trust]
    I -->|invalid or revoked| K[Quarantine]
```

The offline root key signs the public project key registry, while organization manifests carry detached OpenSSH Ed25519 owner signatures. Every project maintains its own isolated Ed25519 signing key. Revocation of any single project key immediately isolates the blast radius without invalidating the broader ecosystem.

## Control Signals & Integrity Metrics

```mermaid
xychart-beta
    title "Verifiable Control Coverage & Invariant Velocity over Time"
    x-axis ["T-12", "T-10", "T-08", "T-06", "T-04", "T-02", "NOW"]
    y-axis "Posture %" 0 --> 100
    bar [18, 34, 56, 72, 85, 97, 100]
    line [12, 30, 54, 75, 88, 98, 100]
```

| Control Signal | Verified State |
| --- | ---: |
| Verified public repositories | **20** |
| Project & owner signing algorithm | **Ed25519** |
| Detached manifest verification | **SHA-256 + OpenSSH `.sig`** |
| Public repositories containing private keys | **0** |
| Private repositories exposed | **0** |
| Private key file mode on managed workstations | **0600** |
| Default trust posture | **Fail-Closed** |

## Architectural Layers & Public Repositories

### 1. Trust & Registry Core (6)

- [safestack-canon](https://github.com/kibernetinio-saugumo-sprendimai/safestack-canon) — Canonical integrity anchors and signed foundational trust principles (archived root anchor).
- [safestack-technical-canon](https://github.com/kibernetinio-saugumo-sprendimai/safestack-technical-canon) — Technical canon specifications, manifest schemas, and cryptographic governance.
- [safestack-project-public-keys](https://github.com/kibernetinio-saugumo-sprendimai/safestack-project-public-keys) — Root-signed public Ed25519 keys for projects and release signers.
- [safestack-validation-registry](https://github.com/kibernetinio-saugumo-sprendimai/safestack-validation-registry) — Official authoritative ledger of validated projects, audit records, and owner-signed declarations.
- [Verification-artifacts](https://github.com/kibernetinio-saugumo-sprendimai/Verification-artifacts) — Detached owner-signed SHA-256 checksum manifests and automated ecosystem verification suite.
- [safestack-control-architecture](https://github.com/kibernetinio-saugumo-sprendimai/safestack-control-architecture) — Layered routing, cryptographic trust boundaries, and control planes.

### 2. Runtime & Infrastructure (4)

- [Safestack-Zero-Trust](https://github.com/kibernetinio-saugumo-sprendimai/Safestack-Zero-Trust) — Local-first zero-trust policy decision engine, default-deny enforcement, and posture gates.
- [SafeStack-Zero-Trust-Platform](https://github.com/kibernetinio-saugumo-sprendimai/SafeStack-Zero-Trust-Platform) — Zero-trust security platform and policy orchestration components.
- [Safestack-Sentinel](https://github.com/kibernetinio-saugumo-sprendimai/Safestack-Sentinel) — Continuous telemetry monitoring daemon and host anomaly detection.
- [Safestack-suite](https://github.com/kibernetinio-saugumo-sprendimai/Safestack-suite) — Integrated runtime utilities and cryptographic CLI tools.

### 3. Intelligence & Automation (2)

- [safestack-audit_system](https://github.com/kibernetinio-saugumo-sprendimai/safestack-audit_system) — Deterministic AI-assisted security audit framework with hardened runtime governance.
- [safestack-OSINT](https://github.com/kibernetinio-saugumo-sprendimai/safestack-OSINT) — Modular, policy-driven OSINT framework with cryptographic integrity verification.

### 4. Web & Publishing (4)

- [freedom.manifesto.github.io](https://github.com/kibernetinio-saugumo-sprendimai/freedom.manifesto.github.io) — Public SafeStack freedom manifesto portal and community documentation.
- [safestack-book](https://github.com/kibernetinio-saugumo-sprendimai/safestack-book) — SafeStack library for architectural books, technical papers, and NIST FIPS standards.
- [safestack-darbu-sauga](https://github.com/kibernetinio-saugumo-sprendimai/safestack-darbu-sauga) — Occupational health and safety (DSS) standard and remote-work ergonomics handbook (`HN 32:2004`).
- [.github](https://github.com/kibernetinio-saugumo-sprendimai/.github) — Global organisation profiles, community health standards, and workflow defaults.

### 5. Ecosystem & Meta (4)

- [safestack-repo-map](https://github.com/kibernetinio-saugumo-sprendimai/safestack-repo-map) — Visual architecture map, repository tree, and machine-readable snapshot of the organisation.
- [safestack-partners](https://github.com/kibernetinio-saugumo-sprendimai/safestack-partners) — Security ecosystem integration resources and partner guidelines.
- [safestack-media-library](https://github.com/kibernetinio-saugumo-sprendimai/safestack-media-library) — Curated visual asset library for schematics, diagrams, and vector assets.
- [safestack-music](https://github.com/kibernetinio-saugumo-sprendimai/safestack-music) — Public SafeStack soundtrack and audio link catalogue.

## Verification First

Public registries and manifests are never trusted merely because they are published. Verify the root-signed project key registry and owner-signed SHA-256 manifests locally:

```bash
# 1. Verify root Ed25519 signature over public-project-keys.json
python3 key_registry.py verify --registry public-project-keys.json

# 2. Verify all ecosystem SHA-256 manifests & detached owner signatures (Verification-artifacts)
./verify.sh
```

All private root, owner, and project keys remain isolated with strict `0600` permissions and are never stored in public repositories. Consult the [registry certificate](https://github.com/kibernetinio-saugumo-sprendimai/safestack-project-public-keys/blob/master/SAFESTACK_PROJECT_PUBLIC_KEYS_CERTIFICATE.md) and [verification artifacts](https://github.com/kibernetinio-saugumo-sprendimai/Verification-artifacts) (`SHA256:jpM7K4+8hyAJo9qg4ISDbljuENZzx2UqMHu73+S9q48`) for current cryptographic anchors.

## Foundational Principles

- **Evidence over claims:** Security controls must produce deterministic, inspectable evidence.
- **Isolation by default:** Failures, credentials, and modules are strictly quarantined to their bounded blast radius.
- **Fail closed:** If a system cannot verify a state or signature, it must refuse to operate.
- **Human review at the boundary:** Automation collects telemetry and drafts audits; human operators decide authoritative state.

<div align="center">
  <sub>SafeStack · Independent security research and systems engineering</sub>
</div>
