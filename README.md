# Vulnerable Test Application

This is a test repository containing intentionally vulnerable dependencies for testing the CodeFabric SCA service with OSV-SCALIBR scanner.

## ⚠️ WARNING
This repository contains **intentionally vulnerable dependencies** for security testing purposes only. 
**DO NOT use these dependencies in production!**

## Vulnerable Dependencies Included

### JavaScript/Node.js (package.json)
- `express@4.17.1` - Multiple CVEs
- `lodash@4.17.19` - Prototype pollution vulnerabilities
- `axios@0.21.1` - SSRF vulnerabilities
- `minimist@1.2.5` - Prototype pollution
- `node-fetch@2.6.0` - Information disclosure
- `ws@7.4.5` - ReDoS vulnerability

### Python (requirements.txt)
- `Django@2.2.0` - SQL injection, XSS vulnerabilities
- `requests@2.20.0` - Security vulnerabilities
- `urllib3@1.24.1` - CRLF injection
- `Pillow@6.2.0` - Buffer overflow vulnerabilities
- `PyYAML@5.1` - Arbitrary code execution
- `cryptography@2.6.1` - Cryptographic vulnerabilities
- `Jinja2@2.10.1` - Sandbox escape
- `Flask@1.0.0` - Security vulnerabilities
- `SQLAlchemy@1.3.0` - SQL injection risks

### Go (go.mod)
- `github.com/gin-gonic/gin@v1.7.0` - Path traversal
- `github.com/gorilla/websocket@v1.4.0` - DoS vulnerabilities
- `github.com/dgrijalva/jwt-go@v3.2.0` - JWT validation bypass
- `gopkg.in/yaml.v2@v2.2.2` - Billion laughs attack
- `github.com/sirupsen/logrus@v1.4.0` - Log injection

## Purpose

This repository is designed to test:
1. OSV-SCALIBR scanner integration
2. Multi-language vulnerability detection
3. SBOM generation from multiple ecosystems
4. Canonical finding normalization
5. Severity scoring and prioritization

## Expected Results

When scanned with OSV-SCALIBR, this repository should detect:
- **50+** total vulnerabilities across all ecosystems
- **Critical** severity findings (CVSS 9.0+)
- **High** severity findings (CVSS 7.0-8.9)
- **Medium** severity findings (CVSS 4.0-6.9)
- Multiple CVE/GHSA identifiers
- Fix versions available for most vulnerabilities

## Usage with CodeFabric

See the parent directory's test scripts for scanning this repository with the CodeFabric SCA service.