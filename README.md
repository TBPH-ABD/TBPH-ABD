<div align="center">

# Salah Abdullah

### Penetration Tester · Web Application Security · Full-Stack Developer

*I build software, then I try to break it — and I write down exactly how.*

[![Email](https://img.shields.io/badge/Email-salahabd.735113%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:salahabd.735113@gmail.com)
[![Location](https://img.shields.io/badge/Based_in-Yemen-006233?style=flat-square&logo=googlemaps&logoColor=white)](#)
[![Focus](https://img.shields.io/badge/Focus-AppSec_%7C_Offensive_Security-0A66C2?style=flat-square&logo=hackthebox&logoColor=white)](#)

</div>

---

## About

Information Technology graduate (**B.Sc., with honors**) specialized in
penetration testing and web application security. I work both sides of the same
problem: I write full-stack applications, and I test applications, APIs, and
networks for the flaws that put them at risk.

Most of what I publish here is **original tooling I wrote myself** — small,
dependency-light, readable programs that each solve one security or engineering
problem well. Offensive recon, blue-team log triage, vulnerability management,
secure-coding references, developer tooling, and IT-support utilities. Every
tool is documented, tested, and reproducible.

-  Currently building **[SecureScope](https://github.com/TBPH-ABD/SecureScope)** — an external attack surface monitoring (EASM) platform for small and mid-sized businesses.
-  Independent **bug bounty hunter** — vulnerability discovery and responsible disclosure on HackerOne, Bugcrowd and Intigriti.
-  Studied toward **CompTIA Security+ (SY0-701)**, **eJPT**, **CEH**, **CompTIA Network+** and **A+** during my degree.
-  I care about the part most people skip: the report. Clear impact, clean reproduction steps, honest severity.

---

## What I Work On

<table>
<tr>
<td width="50%" valign="top">

### Offensive Security
Web application and network penetration testing, API security assessment, and
authorized reconnaissance.

`Broken Access Control (IDOR / BOLA)` · `SQL Injection`
`XSS` · `CSRF` · `Auth & Session Bypass`
`JWT Attacks` · `Security Misconfiguration`

</td>
<td width="50%" valign="top">

### Defensive & Secure Development
Detection engineering, log analysis, file integrity monitoring, static
analysis, and building applications that hold up under review.

`Log Triage` · `FIM` · `SAST` · `Vulnerability Triage (CVSS)`
`Secure Coding` · `CSP / CSRF / PBKDF2`
`Supply-chain (OSV)` · `Reporting`

</td>
</tr>
</table>

---

## Featured Work

###  Flagship

| Project | What it does | Stack |
|---|---|---|
| **[SecureScope](https://github.com/TBPH-ABD/SecureScope)** | External attack surface monitoring (EASM) for SMBs — continuous discovery and risk scoring of internet-facing assets. | TypeScript · Next.js |
| **[security-portfolio](https://github.com/TBPH-ABD/security-portfolio)** | Index of original security and full-stack tools — offensive, defensive, vulnerability management, secure development. | Python |

###  Vulnerability Discovery

| Project | What it does |
|---|---|
| **[jwt-inspector](https://github.com/TBPH-ABD/jwt-inspector)** | Decode a JWT and audit it for `alg:none`, embedded/remote keys, `kid` injection, expiry hygiene, and HMAC verification. |
| **[secret-sweeper](https://github.com/TBPH-ABD/secret-sweeper)** | Find hard-coded secrets in a code tree — vendor key formats plus a Shannon-entropy backstop, with masked output. |
| **[web-recon-scanner](https://github.com/TBPH-ABD/web-recon-scanner)** | Passive web app reconnaissance — security headers, TLS posture, cookie attributes, form surface, information disclosure. |
| **[apitest](https://github.com/TBPH-ABD/apitest)** | REST API security testing — broken authentication, CORS misconfiguration, verbose errors, rate limiting, data exposure. |
| **[recon-mapper](https://github.com/TBPH-ABD/recon-mapper)** | Authorized asset and service discovery — host discovery, concurrent TCP port scanning, banner grabbing, JSON reporting. |

###  Developer & Supply-Chain Tooling

| Project | What it does |
|---|---|
| **[dep-audit](https://github.com/TBPH-ABD/dep-audit)** | Check pinned Python and npm dependencies against the OSV vulnerability database — advisory id, severity, and fixed version. |
| **[pysast](https://github.com/TBPH-ABD/pysast)** | AST-based static analysis for insecure Python — `eval`/`exec`, `shell=True`, unsafe pickle/yaml, `verify=False`, weak hashing. |
| **[cred-audit](https://github.com/TBPH-ABD/cred-audit)** | Credential policy auditing based on real offline-cracking resistance, with privacy-preserving breach-corpus checks. |

###  Defensive & Monitoring

| Project | What it does |
|---|---|
| **[sentinel-log-analyzer](https://github.com/TBPH-ABD/sentinel-log-analyzer)** | Blue-team log triage — SSH brute force, credential compromise, content discovery scans, web attack patterns. |
| **[integrity-guard](https://github.com/TBPH-ABD/integrity-guard)** | File integrity monitoring — cryptographic baselining with detection of added, modified, deleted and re-permissioned files. |
| **[phishguard](https://github.com/TBPH-ABD/phishguard)** | Phishing URL analysis — typosquatting, homoglyph and punycode deception, credential lures, redirect-chain tracing. |
| **[vulnfeed](https://github.com/TBPH-ABD/vulnfeed)** | CVE lookup and triage CLI backed by the NIST NVD — severity filtering, network-exploitability flags, local caching. |

###  IT Support & Full-Stack

| Project | What it does |
|---|---|
| **[sysdoctor](https://github.com/TBPH-ABD/sysdoctor)** | Read-only machine & connectivity health check — disk, load, DNS, TCP and HTTP probes with a PASS/WARN/FAIL report and JSON. |
| **[helpdesk-lite](https://github.com/TBPH-ABD/helpdesk-lite)** | Self-contained support ticket system (HTML + JSON API, SQLite) demonstrating secure web coding end-to-end. |
| **[netwatch](https://github.com/TBPH-ABD/netwatch)** | Network service monitoring with a live dashboard, SQLite history and JSON API — standard library alone. |
| **[securenotes](https://github.com/TBPH-ABD/securenotes)** | A notes app written to demonstrate secure coding: PBKDF2 hashing, hashed session tokens, CSRF protection, IDOR-safe queries, strict CSP. |

---

## Engineering Standards

Every tool in these repositories follows the same bar:

- **Zero runtime dependencies** — the security and IT tools run on the Python
  standard library alone. Fewer dependencies, fewer surprises, easier to audit.
- **Tested** — each tool ships with a `unittest` suite (no third-party test
  framework), and tests never touch a real external service.
- **CI on every push** — GitHub Actions runs the suite across Python
  3.10–3.13, a `-W error::ResourceWarning` pass, a coverage gate, and a syntax
  check.
- **Authorized use only** — anything that touches a remote target carries an
  explicit authorization notice. Responsible disclosure is the job, not a
  formality.

---

## Toolchain

**Security**
<br>
![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=flat-square&logo=burpsuite&logoColor=white)
![Metasploit](https://img.shields.io/badge/Metasploit-2596CD?style=flat-square&logo=metasploit&logoColor=white)
![Nmap](https://img.shields.io/badge/Nmap-4682B4?style=flat-square&logo=gnometerminal&logoColor=white)
![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white)
![Kali](https://img.shields.io/badge/Kali_Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white)
![sqlmap](https://img.shields.io/badge/sqlmap-CC0000?style=flat-square&logo=databricks&logoColor=white)
![Nessus](https://img.shields.io/badge/Nessus-00C176?style=flat-square&logo=tenable&logoColor=white)
![OWASP ZAP](https://img.shields.io/badge/OWASP_ZAP-00549E?style=flat-square&logo=owasp&logoColor=white)
![Nuclei](https://img.shields.io/badge/Nuclei-1E90FF?style=flat-square&logo=projectdiscovery&logoColor=white)

**Engineering**
<br>
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

---

## Education

**B.Sc. in Information Technology** — University of Science and Technology · 2025–2026
Graduated with honors. Graduation project graded *excellent*: a device
access-recovery tool. Coursework and self-study across penetration testing
(Security+, eJPT, CEH) and IT support & systems administration (Network+, A+).

---

<div align="center">

### 📊 Activity

![Stats](https://github-readme-stats.vercel.app/api?username=TBPH-ABD&show_icons=true&hide_border=true&theme=default&count_private=true)
![Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=TBPH-ABD&layout=compact&hide_border=true&theme=default&langs_count=8)

---

**Open to penetration testing, application security, IT, and software engineering roles.**

[![Email](https://img.shields.io/badge/Get_in_touch-salahabd.735113%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:salahabd.735113@gmail.com)

*Languages: Arabic (native) · English (fluent)*

</div>
