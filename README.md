 ecoScan4x | HTTP Security Header Auditor 🛡️

 📌 Project Overview
ecoScan4x is a lightweight Python-based reconnaissance tool designed to evaluate the security posture of web applications. It automates the inspection of HTTP response headers to identify misconfigurations that leave websites vulnerable to common attack vectors.

This tool is built to align with ISO/IEC 27001 Annex A.12 (Operations Security) and OWASP Top 10 standards.

🚀 Key Features
- Automated Risk Assessment: Categorizes missing headers into High, Medium, and Low risk levels.
- Compliance Alignment: Specifically checks for HSTS, CSP, and X-Frame-Options.
- Audit Logging: Automatically generates timestamped JSON reports for compliance documentation.
- Bulk Scanning: Supports scanning single URLs or multiple targets from a text file.

 🛡️ Security Impact (Risks Mitigated)
- Content-Security-Policy (CSP): Prevents Cross-Site Scripting (XSS) and data injection attacks.
- Strict-Transport-Security (HSTS): Mitigates Man-in-the-Middle (MitM) and SSL Stripping.
- X-Frame-Options: Blocks Clickjacking attempts by controlling iframe embedding.
- X-Content-Type-Options: Prevents MIME-type sniffing exploits.

 💻 Installation & Usage
 Prerequisites
- Python 3.x
- `requests` library

```bash
pip install requests

1. Scan a Single Target
Bash
python ecoScan4x.py [https://example.com](https://example.com)

2. Bulk Scan from File
Bash
python ecoScan4x.py targets.txt

📋 Sample Output (JSON Audit Log)
JSON
{
    "url": "[https://example.com](https://example.com)",
    "risk_level": "CRITICAL",
    "missing_headers": [
        {"header": "Content-Security-Policy", "risk": "High"},
        {"header": "Strict-Transport-Security", "risk": "High"}
    ],
    "https_verified": true
}


⚠️ Disclaimer
This tool is for educational and authorized security auditing purposes only. Unauthorized scanning of third-party assets may be illegal.
