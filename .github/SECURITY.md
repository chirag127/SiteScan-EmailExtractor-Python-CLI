# Security Policy for AquaScout-Web-Email-Extractor-CLI-Tool

As the Apex Technical Authority, we treat security with the highest priority. This repository, **AquaScout-Web-Email-Extractor-CLI-Tool**, is designed for robust, controlled data extraction tasks. We maintain future-proof standards based on the wisdom of Managing the Unmanageable.

## 1. Supported Versions

We actively support the latest stable release branch of Python (currently **Python 3.12+** per late 2025 standards) and all directly dependent packages managed via `uv`.

| Version | Status | Deployment Target |
| :--- | :--- | :--- |
| Latest Stable | Supported | Deployed/Tested |
| N/A (Legacy) | Security Fixes Only | Next Major Release Removal |

## 2. Reporting a Vulnerability

We adhere to a strict, rapid response protocol for security disclosures. If you discover any vulnerability in **AquaScout-Web-Email-Extractor-CLI-Tool**, please follow these steps immediately:

1.  **DO NOT** open a public issue. Unauthorized disclosure compromises the integrity of our users.
2.  **Private Disclosure:** Send a detailed, encrypted report (if possible) directly to the security contact: `security+aquascout@chirag127.com` (Placeholder email; actual security contact procedures should be established).
3.  **Content:** Your report must include:
    *   A clear description of the vulnerability.
    *   Steps to reproduce (PoC).
    *   The affected component (e.g., `urllib3` dependency, core parsing logic).
    *   Your contact information (optional, but recommended for follow-up).

## 3. Disclosure Timeline & Remediation

Upon receipt of a valid security report, the Apex Team commits to the following timeline:

| Action | Target SLA | Notes |
| :--- | :--- | :--- |
| Acknowledge Receipt | Within 12 Hours | Confirmation of receipt and initial triage. |
| Initial Assessment | Within 48 Hours | Determining severity and scope. |
| Fix Development | TBD based on severity (Max 7 Days) | Applying patches adhering to SOLID/DRY principles. |
| Private Patch Release | Before Public Disclosure | Deploying fix internally for final verification. |
| Public Disclosure | Coordinated with Fix Release | Issuing an advisory and releasing the patched version via GitHub and PyPI. |

## 4. Security Best Practices in Development

Our Python development adheres to rigorous standards defined in our **AGENTS.md** directives:

*   **Dependency Management:** All dependencies are managed via `uv` and scanned using industry-standard SCA tools integrated into our **CI/CD pipeline (`.github/workflows/ci.yml`)**.
*   **Input Sanitization:** Because this is a web crawler, all scraped data is treated as untrusted input. Data handlers strictly use **Ruff** rules to enforce safe string handling and prevent injection vectors, even if the primary use case is output logging.
*   **Secrets Management:** No secrets (API keys, tokens) are ever committed to the repository. All required credentials for external services (e.g., hosting platforms, advanced AI services) must be injected via secure GitHub Actions secrets or environment variables.
*   **Configuration Integrity:** Configuration files are validated against a strict schema (`click` validation layers) to ensure the integrity of operational parameters, preventing misconfigurations that could lead to Denial of Service or over-crawling.

--- 

*This security policy is maintained under the governance model established by the Apex Technical Authority.*