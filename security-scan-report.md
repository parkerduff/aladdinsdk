# Security Scan Report: parkerduff/aladdinsdk

**Branch:** `devin/security-scan-1778691197`  
**Date:** 2026-05-13  

## Tools Used

| # | Tool | Type | Findings |
|---|------|------|----------|
| 1 | **pip-audit** v2.9.0 | Dependency CVE scanner (PyPI advisory DB) | 29 vulns across 12 packages |
| 2 | **Safety** v2.3.5 | Dependency vulnerability scanner (SafetyCLI DB) | 24 vulns across 10 packages |
| 3 | **Bandit** v1.8.6 | Python static security analysis (SAST) | 50 code-level issues (CWE-mapped) |
| 4 | **Grype** v0.112.0 | General vulnerability scanner (Anchore DB) | 29 vulns across 11 packages |

> **Note:** Trivy v0.70.0 was also run but could not detect packages (no `site-packages` in the scanned directory). Its results are excluded.

---

## Consolidated CVE / Vulnerability List (33 unique entries)

### cryptography==42.0.8 (4 vulnerabilities)

| CVE | GHSA | Fix Version | Detected By |
|-----|------|-------------|-------------|
| CVE-2024-12797 | GHSA-79v4-65xg-pq4g | 44.0.1 | pip-audit, safety, grype |
| CVE-2026-26007 | GHSA-r6ph-v2qm-q3c2 | 46.0.5 | pip-audit, safety, grype |
| CVE-2026-34073 | GHSA-m959-cc7f-wv43 | 46.0.6 | pip-audit, safety, grype |
| — | GHSA-h4gh-qq45-vh27 | 43.0.1 | pip-audit, safety, grype |

**Recommendation:** Upgrade to `cryptography>=46.0.6`

### filelock==3.19.1 (2 vulnerabilities)

| CVE | GHSA | Fix Version | Detected By |
|-----|------|-------------|-------------|
| CVE-2025-68146 | GHSA-w853-jp5j-5j7f | 3.20.1 | pip-audit, safety, grype |
| CVE-2026-22701 | GHSA-qmgc-5h2g-mvrw | 3.20.3 | pip-audit, safety, grype |

**Recommendation:** Upgrade to `filelock>=3.20.3`

### marshmallow==4.0.1 (1 vulnerability)

| CVE | GHSA | Fix Version | Detected By |
|-----|------|-------------|-------------|
| CVE-2025-68480 | GHSA-428g-f7cq-pgp5 | 4.1.2 | pip-audit, safety, grype |

**Recommendation:** Upgrade to `marshmallow>=4.1.2`

### nltk==3.9.2 (8 vulnerabilities — highest-risk package)

| CVE | GHSA | Fix Version | Detected By |
|-----|------|-------------|-------------|
| CVE-2025-14009 | GHSA-7p94-766c-hgjp | 3.9.3 | pip-audit, safety, grype |
| CVE-2026-0846 | GHSA-h8wq-7xc4-p3qx | 3.9.3 | pip-audit, safety, grype |
| CVE-2026-0847 | GHSA-68j8-pq59-fqgm | — (no fix) | pip-audit, safety, grype |
| CVE-2026-33230 | GHSA-gfwx-w7gr-fvh7 | 3.9.4 | pip-audit, safety, grype |
| CVE-2026-33231 | GHSA-jm6w-m3j8-898g | 3.9.4 | pip-audit, safety, grype |
| CVE-2026-33236 | — | — | safety |
| — | GHSA-rf74-v2fm-23pw | — (no fix) | pip-audit, safety, grype |
| — | GHSA-469j-vmhf-r6v7 | — (no fix) | grype |

**Recommendation:** Upgrade to `nltk>=3.9.4` (3 vulns still have no fix)

### pip==26.0.1 (2 vulnerabilities)

| CVE | GHSA | Fix Version | Detected By |
|-----|------|-------------|-------------|
| CVE-2026-3219 | GHSA-58qw-9mgm-455v | — (no fix) | pip-audit, grype |
| CVE-2026-6357 | GHSA-jp4c-xjxw-mgf9 | 26.1 | pip-audit, grype |

**Recommendation:** Upgrade to `pip>=26.1`

### pyopenssl==24.0.0 (2 vulnerabilities)

| CVE | GHSA | Fix Version | Detected By |
|-----|------|-------------|-------------|
| CVE-2026-27448 | GHSA-vp96-hxj8-p424 | 26.0.0 | pip-audit, safety, grype |
| CVE-2026-27459 | GHSA-5pwr-322w-8jr4 | 26.0.0 | pip-audit, safety, grype |

**Recommendation:** Upgrade to `pyopenssl>=26.0.0`

### pytest==8.4.2 (1 vulnerability)

| CVE | GHSA | Fix Version | Detected By |
|-----|------|-------------|-------------|
| CVE-2025-71176 | GHSA-6w46-j5rx-g56g | 9.0.3 | pip-audit, safety, grype |

**Recommendation:** Upgrade to `pytest>=9.0.3` (dev dependency only)

### requests==2.32.5 (1 vulnerability)

| CVE | GHSA | Fix Version | Detected By |
|-----|------|-------------|-------------|
| CVE-2026-25645 | GHSA-gc5v-m9x4-r6x2 | 2.33.0 | pip-audit, safety, grype |

**Recommendation:** Upgrade to `requests>=2.33.0`

### setuptools==58.1.0 (5 vulnerabilities)

| CVE | GHSA | Fix Version | Detected By |
|-----|------|-------------|-------------|
| CVE-2022-40897 | PYSEC-2022-43012 | 65.5.1 | pip-audit |
| CVE-2024-6345 | GHSA-cx63-2mw6-8hw5 | 70.0.0 | pip-audit, grype |
| CVE-2025-47273 | GHSA-5rjg-fvgr-3xxf | 78.1.1 | pip-audit, grype |
| — | GHSA-r9hx-vwmv-q579 | 65.5.1 | grype |

**Recommendation:** Upgrade to `setuptools>=78.1.1`

### snowflake-connector-python==3.17.3 (1 vulnerability)

| CVE | Advisory | Fix Version | Detected By |
|-----|----------|-------------|-------------|
| — | Safety-80257 (Insecure File Permissions) | — | safety |

**Recommendation:** Check for latest snowflake-connector-python release

### urllib3==1.26.20 (5 vulnerabilities)

| CVE | GHSA | Fix Version | Detected By |
|-----|------|-------------|-------------|
| CVE-2025-50181 | GHSA-pq67-6m6q-mj2v | 2.5.0 | pip-audit, safety, grype |
| CVE-2025-66418 | GHSA-gm62-xv2j-4w53 | 2.6.0 | pip-audit, safety, grype |
| CVE-2025-66471 | GHSA-2xpw-w6gg-jr37 | 2.6.0 | pip-audit, safety, grype |
| CVE-2026-21441 | GHSA-38jv-5279-wg99 | 2.6.3 | pip-audit, safety, grype |
| CVE-2026-44431 | GHSA-qccp-gfcp-xxvc | 2.7.0 | pip-audit, grype |

**Recommendation:** Upgrade to `urllib3>=2.7.0` (⚠️ major version change — breaking API changes)

### pypa/gh-action-pypi-publish (GitHub Action)

| CVE | GHSA | Fix Version | Detected By |
|-----|------|-------------|-------------|
| — | GHSA-vxmw-7h4f-hqxh | 1.13.0 | grype |

**Recommendation:** Update GitHub Action to `v1.13.0+`

---

## Bandit Static Analysis Summary (50 issues)

| Severity | Count | Key CWEs |
|----------|-------|----------|
| MEDIUM | 10 | CWE-78 (OS Command Injection via `eval`), CWE-400 (DoS via missing request timeout), CWE-502 (Pickle deserialization) |
| LOW | 40 | CWE-259 (Hardcoded passwords/credential patterns), CWE-703 (Use of `assert`) |

Notable MEDIUM findings:
- **CWE-78**: `eval()` usage in `aladdinsdk/common/authentication/api.py` (lines 295, 303, 310)
- **CWE-400**: HTTP requests without timeout in 5 locations across OAuth clients
- **CWE-502**: Pickle usage in `aladdinsdk/common/exports/utils/write_file_util.py`

---

## Summary

- **33 unique dependency vulnerabilities** across 11 packages (+ 1 GitHub Action)
- **50 static analysis issues** (10 MEDIUM, 40 LOW)
- **Highest-risk packages**: `nltk` (8 vulns, 3 unfixed), `urllib3` (5 vulns), `setuptools` (5 vulns), `cryptography` (4 vulns)
- **Most critical upgrades needed**: `cryptography`, `urllib3`, `setuptools`, `pyopenssl`, `nltk`
