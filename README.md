# .signal.fyi – MVP1: Embedded Compliance Evidence

This repository demonstrates how Signal.fyi generates daily, Git-native compliance artifacts for container-based projects.

An example report teams can expect to see will start from here nested in the same directory structure we will provide for clients with our daily scans. [View Compliance Report](compliance/README.md)

## 🎯 Purpose

Signal.fyi commits machine-readable and human-readable compliance evidence **directly into source control**. This makes it possible for security, engineering, and compliance teams to operate from a shared source of truth — without dashboards, portals, or context-switching.

This is an early MVP scoped to tracking the security posture of a repository's **parent Docker image** (e.g. `python:latest`) and surfacing relevant compliance signals.

---

## 📂 What's Inside `.signal.fyi/compliance/`

The `.signal.fyi/compliance/` directory contains **everything needed to pass key controls** from SOC 2, ISO 27001, and HIPAA related to vulnerability management.

```
.signal.fyi/
└── compliance/
    ├── compliance.md            ← ✅ One-stop, human-readable summary
    ├── compliance_bundle.zip    ← 🔒 Optional: export everything for audits
    ├── soc2/
    │   └── cc7.1.md             ← SOC 2: Evidence for vulnerability scanning
    ├── iso27001/
    │   └── a.12.6.1.md          ← ISO 27001: Technical vulnerability mgmt
    ├── hipaa/
    │   └── 164.308a8.md         ← HIPAA: Security management process
    └── provenance/
        ├── sbom.json           ← Machine-readable SBOM (CycloneDX v1.6)
        ├── cve-summary.json    ← Raw CVE data from Trivy
        └── metadata.json       ← Digest, timestamp, scan tool version
```

---

## ✅ What This Enables

| Role             | Value Delivered                                                                 |
|------------------|----------------------------------------------------------------------------------|
| **GRC/Compliance** | Daily timestamped evidence for SOC 2, ISO 27001, and HIPAA audits              |
| **Security**     | No need to manually track parent image vulnerabilities or scan history          |
| **Engineering**  | Minimal friction — no need to change workflow or open new tools                 |
| **Auditors**     | Direct commit trail showing when scans ran and what evidence was generated      |

---

## 🔍 Use Case Example

This example tracks `python:latest` as the base image. Every day, Signal.fyi:

1. Scans the image using **Trivy**
2. Generates:
   - A **CycloneDX SBOM**
   - A **CVE summary**
   - A **timestamped metadata file**
3. Updates `compliance.md` with:
   - Scan date
   - Status (pass/fail)
   - Evidence links
4. Writes markdown files for each compliance control with explanations

---

## 🛠 Tools Used

- [`Trivy`](https://github.com/aquasecurity/trivy) for vulnerability scanning and SBOM generation
- [`CycloneDX`](https://cyclonedx.org/) v1.6 format for SBOMs
- Native GitHub commit trail for verifiable timestamps

---

## 🔜 Coming Next

- Full multi-stage Dockerfile support
- VEX + TEA integration for richer context
- OSCAL and NIST mappings for FedRAMP and beyond

---

This is MVP1. Our goal is simple: **make compliance visible, automated, and frictionless — starting with your container base image.**
