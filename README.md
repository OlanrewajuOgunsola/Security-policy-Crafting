# Cybersecurity Policy Framework Project

## 🏢 MSHS case study
**MedSecure Health Systems (MSHS)** is a mid-sized healthcare technology provider.  
They specialize in developing electronic medical record (EMR) platforms, cloud-hosted patient portals, and connected diagnostic devices for hospitals and clinics.  

### Business Context
- **Industry**: Healthcare IT / Cloud Services  
- **Size**: 500 employees, multiple data centers, and AWS-based cloud workloads  
- **Critical Assets**: Patient health records (PHI), EMR databases, medical IoT devices, cloud infrastructure  
- **Regulatory Drivers**: HIPAA, GDPR, NIST Cybersecurity Framework, ISO 27001  

### Security Challenges
MSHS identified several gaps in their **governance and security controls**:
- Employees lacked clear guidelines on acceptable system and internet use.  
- Database credentials were inconsistently managed and shared among developers.  
- Network devices (routers, switches, firewalls) were configured ad hoc with weak change controls.  
- Cloud workloads in AWS and Azure were being provisioned without proper vendor risk evaluation.  
- Internal network access lacked consistent segmentation and least-privilege enforcement.  
- Vulnerability scanning was ad hoc and patch cycles inconsistent.  
- Encryption practices varied between teams with no defined standards.  

---

## Project Deliverables
The following policies were developed as part of the **Cybersecurity Policy Framework**:

1. **Acceptable Use Standard Policy**  
   - Defines acceptable and prohibited behaviors when using company IT assets (email, internet, devices, cloud apps).  
   - Covers monitoring, privacy expectations, and disciplinary actions for violations.  

2. **Database Credentials Policy**  
   - Enforces unique, non-shared database credentials.  
   - Requires credential vaulting (e.g., HashiCorp Vault, AWS Secrets Manager).  
   - Mandates rotation every 90 days and MFA for admin accounts.  

3. **Network Device Management Policy**  
   - Standardizes configuration baselines for routers, switches, firewalls.  
   - Defines backup, patching, logging, and secure access methods (SSH v2, no Telnet).  
   - Enforces change control via a centralized management system.  

4. **Cloud Service Provider (CSP) Management Policy**  
   - Establishes vendor due diligence process (security questionnaires, certifications).  
   - Defines data residency and encryption requirements for cloud services.  
   - Requires contract clauses on incident response and breach notifications.  

5. **Internal Network Access Management Policy**  
   - Defines VLAN segmentation for production, testing, guest, and IoT networks.  
   - Enforces least privilege via RBAC and NAC solutions.  
   - Requires MFA for remote VPN access.  

6. **Vulnerability Management Policy**  
   - Requires monthly vulnerability scans across endpoints, servers, cloud, and IoT devices.  
   - Defines SLAs for remediation:  
     - Critical: 7 days  
     - High: 14 days  
     - Medium: 30 days  
     - Low: 60 days  
   - Requires tracking via a centralized vulnerability management platform.  

7. **Acceptable Encryption Standard**  
   - Defines approved algorithms (AES-256, RSA-2048+, SHA-256, TLS 1.2/1.3).  
   - Prohibits outdated protocols (SSL, TLS 1.0/1.1, MD5, DES).  
   - Requires encryption at rest and in transit for all PHI and sensitive data.  

---

## Tools & References
- **Frameworks**: NIST CSF, ISO 27001, HIPAA Security Rule  
- **Tools**: Nessus / OpenVAS (vulnerability scanning), AWS IAM + Secrets Manager, Cisco ISE (network access), HashiCorp Vault  
- **Best Practices**: CIS Benchmarks, OWASP ASVS  

---

## 📂 Repo Structure
