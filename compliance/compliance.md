# Compliance Evidence Summary

This repository contains daily compliance evidence for the parent Docker image `python:latest`.

## 📅 Scan Info
- **Image Digest:** `sha256:...`
- **Scan Timestamp (UTC):** `2025-06-05T04:00:12Z`
- **Trivy Version:** `0.51.1`
- **SBOM Format:** CycloneDX v1.6
- **Scan Result:** ✅ No Critical Vulnerabilities

## ✅ Compliance Snapshot

| Framework  | Control                                | Status | Evidence |
|------------|----------------------------------------|--------|----------|
| SOC 2      | CC7.1 – Vulnerability Management        | ✅ Pass | [cc7.1.md](soc2/cc7.1.md) |
| ISO 27001  | A.12.6.1 – Technical Vulnerability Mgmt | ✅ Pass | [a.12.6.1.md](iso27001/a.12.6.1.md) |
| HIPAA      | 164.308(a)(8) – Security Mgmt Process   | ✅ Pass | [164.308a8.md](hipaa/164.308a8.md) |

Each control is supported by machine-readable artifacts available in the [`provenance/`](provenance/) folder:
- [sbom.json](provenance/sbom.json)
- [cve-summary.json](provenance/cve-summary.json)
- [metadata.json](provenance/metadata.json)

---

## 🧪 Summary Judgment
This scan passed all mapped controls for `python:latest`.
If you are a compliance official, you may:
- Review control evidence linked above
- Download all files for offline audit ([compliance_bundle.zip](compliance_bundle.zip))

For questions or validation assistance, contact your engineering or security lead.
