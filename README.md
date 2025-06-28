# CyberSecurity_Task-3

# OpenVAS Vulnerability Assessment Summary

This repository contains a summary of a vulnerability assessment conducted using OpenVAS for the host `192.168.1.109`.

## Scan Details

- **Tool**: OpenVAS (HackerTarget)
- **Date**: June 27, 2025
- **Target**: 192.168.1.109
- **Findings**:
  - High severity: 18
  - Medium severity: 36
  - Low severity: 3

## Summary of Key Issues

### High Severity
- Outdated OS: Ubuntu 8.04 (end of life)
- Multiple services (MySQL, PostgreSQL, SSH, VNC) using weak or default credentials
- Remote code execution via Distributed Ruby, Java RMI, DistCC
- Backdoors detected in vsftpd and UnrealIRCd
- Web vulnerabilities: XSS, command execution, unsafe HTTP methods, exposed phpinfo

### Medium Severity
- Anonymous FTP access
- Expired SSL certificates, weak TLS configurations
- Insecure protocols and services (FTP, Telnet, VNC)
- SQL injection and CSRF in TWiki and Tiki Wiki
- Directory browsing and exposed debug methods

### Low Severity
- TCP timestamps enabled
- Weak SSH MAC algorithms

## Recommendations

- Upgrade OS and all outdated software
- Enforce strong passwords and disable default credentials
- Remove or secure exposed services and web files
- Apply SSL/TLS best practices and renew certificates
- Disable unnecessary protocols and methods (e.g., TRACE, PUT)

## File

- `open_vas_vulnerability_report.pdf`: Full scan report
