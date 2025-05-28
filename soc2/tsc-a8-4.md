# SOC 2 – A.8.4 Secure Development Policy

**Requirement:** Develop code securely with deterministic dependencies.

**Evidence:**
- `FROM python:3.10-slim@sha256:abc...` in `/Dockerfile`
- Pinned digest prevents image drift across builds
- File committed and tracked in Git history

**Artifacts:**
- [SBOM](../../sbom/sbom-python-3.10.json)
- [Dockerfile](../../Dockerfile)
