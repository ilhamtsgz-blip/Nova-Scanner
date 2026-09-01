
# 🛡️ CYBERNOVA SECURITY GATEWAY
## DEV ILHAMGZ AI SECURITY SCANNER v3.0.0

<div align="center">
  
![Version](https://img.shields.io/badge/version-3.0.0-blue)
![Python](https://img.shields.io/badge/python-3.8%2B-green)
![License](https://img.shields.io/badge/license-MIT-red)
![Security](https://img.shields.io/badge/security-passive-yellow)

**Premium Passive Web Security Assessment Framework**

[Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Configuration](#-configuration) • [Security](#-security)

</div>

---

## 📋 **DESCRIPTION**

**DEV ILHAMGZ AI SECURITY SCANNER** adalah tool keamanan web passive yang canggih untuk melakukan security assessment pada sistem yang Anda miliki atau memiliki izin untuk menguji. Tool ini dilindungi oleh **CyberNova Security Gateway** yang memastikan hanya pengguna terdaftar yang dapat mengaksesnya.

### 🎯 **Tujuan**
- Melakukan passive security assessment secara aman dan terkontrol
- Mendeteksi berbagai jenis kelemahan keamanan web
- Memberikan laporan yang komprehensif dan mudah dipahami
- Dilindungi dengan sistem autentikasi berbasis ID

---

## ✨ **FEATURES**

### 🔐 **Security Gateway**
- ✅ **ID-Based Authentication** - Setiap pengguna memiliki ID unik
- ✅ **GitHub Verification** - Verifikasi ID melalui GitHub raw
- ✅ **Telegram Notifications** - Notifikasi real-time ke owner
- ✅ **Local Cache** - Penyimpanan ID lokal untuk offline access
- ✅ **Anti-Tamper** - Proteksi dari eksekusi langsung

### 🚀 **Scanner Features**
- ✅ **HTTP/HTTPS Analysis** - Redirect detection, mixed content
- ✅ **Security Headers** - CSP, HSTS, XFO, X-Content-Type-Options, dll
- ✅ **Cookie Analysis** - Secure, HttpOnly, SameSite detection
- ✅ **CORS Analysis** - Wildcard, credentials, methods
- ✅ **Subdomain Enumeration** - Passive discovery from public sources
- ✅ **SSL/TLS Analysis** - Certificate validation, weak ciphers
- ✅ **CVE Lookup** - Vulnerability matching for detected technologies
- ✅ **JavaScript Analysis** - API endpoints, secrets, source maps
- ✅ **Form Security Analysis** - CSRF tokens, password fields
- ✅ **Information Disclosure** - Stack traces, internal paths
- ✅ **Technology Fingerprinting** - Detect frameworks and versions
- ✅ **AI-Powered Analysis** - Gemini 3.6 Flash integration
- ✅ **Multiple Report Formats** - TXT, JSON, HTML, SARIF, JUnit
- ✅ **Rich Terminal UI** - Beautiful and informative interface

---

## 📁 **PROJECT STRUCTURE**

```

project/
├── main.py                          # CyberNova Security Gateway (Entry Point)
├── CYBERNOVA/
│   └── dev_ilhamgz.py              # DEV ILHAMGZ AI Security Scanner
├── requirements.txt                 # Python dependencies
└──README.md 

```

---

## 🔧 **INSTALLATION**

### 1. **Clone Repository**
```bash
git clone https://github.com/blip-ilhamgz/Nova-scanner
cd Nova-scanner
```

2. Install Dependencies

```bash
pip install -r requirements.txt
```

---

🚀 USAGE

Basic Usage

1. Jalankan Security Gateway

```bash
python3 main.py
```

2. Register (Pertama Kali)

```bash
python3 main.py --register
```

3. Cek Status Authorization

```bash
python3 main.py --status
```

---

Scanning Commands

Quick Scan (Full Assessment)

```bash
python3 main.py --target https://example.com --mode quick
```

Reconnaissance

```bash
python3 main.py --target https://example.com --mode recon
```

HTTP Header Analysis

```bash
python3 main.py --target https://example.com --mode headers
```

Endpoint Discovery

```bash
python3 main.py --target https://example.com --mode endpoints
```

JavaScript Analysis

```bash
python3 main.py --target https://example.com --mode js
```

Cookie Security Analysis

```bash
python3 main.py --target https://example.com --mode cookies
```

CORS Analysis

```bash
python3 main.py --target https://example.com --mode cors
```

Security Configuration Check

```bash
python3 main.py --target https://example.com --mode security
```

Subdomain Enumeration

```bash
python3 main.py --target example.com --mode subdomain
```

SSL/TLS Analysis

```bash
python3 main.py --target example.com --mode ssl
```

AI-Powered Analysis

```bash
python3 main.py --target https://example.com --mode ai
```

---

Generate Reports

TXT Report

```bash
python3 main.py --target https://example.com --report txt -o report.txt
```

JSON Report

```bash
python3 main.py --target https://example.com --report json -o report.json
```

HTML Report

```bash
python3 main.py --target https://example.com --report html -o report.html
```

SARIF Report (Static Analysis)

```bash
python3 main.py --target https://example.com --report sarif -o report.sarif
```

JUnit Report (CI/CD)

```bash
python3 main.py --target https://example.com --report junit -o report.xml
```

---

Advanced Options

Option Description Example
--timeout Request timeout (seconds) --timeout 30
--workers Max concurrent workers --workers 5
--delay Delay between requests --delay 0.5
--no-ai Disable AI analysis --no-ai
--quiet Quiet mode (less output) --quiet
--verbose Verbose mode (more output) --verbose

---

Complete Example

```bash
python3 main.py --target https://example.com --mode quick --report html -o report.html --timeout 20 --workers 5
```

---

🔐 SECURITY

Authorization Flow

```
User runs main.py
       ↓
Check local ID (~/.cybernova_id.dat)
       ↓
    [No ID] → Generate ID → Register → Notify Owner
       ↓
    [Has ID] → Fetch authorized IDs from GitHub
       ↓
    [Valid] → ✅ Access Granted → Run Scanner
       ↓
  [Invalid] → ❌ Access Denied
```

Security Features

1. ID-Based Authentication - Setiap user memiliki ID unik
2. Hardware Binding - ID terikat dengan hardware device
3. GitHub Verification - Verifikasi real-time dari GitHub
4. Telegram Notifications - Notifikasi ke owner untuk setiap request
5. Local Cache - Offline access untuk user terdaftar
6. Anti-Tamper - Proteksi dari eksekusi langsung

Why This Security?

· Prevents Unauthorized Access - Hanya user terdaftar yang bisa menggunakan
· Owner Control - Owner dapat menambah/menghapus user kapan saja
· Audit Trail - Semua request tercatat via Telegram
· No Hardcoded Credentials - Semua verifikasi via GitHub

---

📊 FINDING TYPES

Severity Description Example
CRITICAL Immediate action required HTTP without HTTPS, SSL expired
HIGH Serious vulnerability Password form over HTTP
MEDIUM Moderate risk Weak HSTS, Missing security headers
LOW Low risk Server version disclosure
INFO Informational Technology detected

Finding Status

· ✅ Confirmed - Evidence is strong
· ⚠️ Potential - Need verification
· ℹ️ Informational - Non-vulnerability
· ❌ False Positive - Not actually vulnerable

---

📄 REPORT FORMATS

TXT

Plain text report with complete details.

JSON

Structured data for programmatic processing:

```json
{
  "scanner": {"name": "DEV ILHAMGZ", "version": "3.0.0"},
  "target": {"url": "https://example.com"},
  "findings": [...]
}
```

HTML

Professional web report with:

· Dashboard summary
· Severity cards
· Finding details
· Premium features
· Responsive design

SARIF

Static Analysis Results Interchange Format for CI/CD integration.

JUnit

JUnit XML format for Jenkins/GitLab CI integration.

---

🛠️ DEPENDENCIES

Required

· Python 3.8+
· requests
· rich

Optional (for premium features)

· dnspython - DNS analysis
· cryptography - SSL/TLS analysis
· whois - WHOIS lookup
· selenium - Screenshots (requires Chrome/Chromium)

---

📝 LICENSE

MIT License - See LICENSE file for details.

---

👨‍💻 DEVELOPER

Dev IlhamGZ

· GitHub: @ilhamtsgz-blip
· Telegram: @ilhamtsgz
· Project: CyberNova Security

---

⚠️ DISCLAIMER

This tool is for authorized security testing only!

· Only scan systems you own or have explicit written permission to test
· This tool performs passive/low-impact assessment only
· No exploitation or destructive testing is performed
· The developer is not responsible for misuse of this tool
· Always comply with local laws and regulations

---

🔄 VERSION HISTORY

Version Date Changes
3.0.0 2024 Premium features, Security Gateway, Multiple formats
2.2.0 2023 Enhanced analysis, AI integration
2.1.0 2023 Added CORS, Cookie analysis
2.0.0 2023 Major refactor, Rich UI

---

🤝 CONTRIBUTING

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch
3. Submit a pull request

---

📞 CONTACT

· Owner: CyberNova
· Contact: @ilhamtsgz
· Email: [ilhamtsgz@gmail.com]

---

<div align="center">

Made with ❤️ by Dev IlhamGZ

⬆ Back to Top
