# Security Audit Report – Small Enterprise Environment

## 1. Objective
The objective of this audit is to assess the security posture of a small enterprise IT environment, identify potential risks, and recommend appropriate controls aligned with industry best practices.

---

## 2. Scope
This audit considers a small organisation with the following environment:
- 25 employees
- Cloud-based email system (e.g. Microsoft 365)
- Shared file storage
- Basic internal network
- No dedicated security team

The assessment focuses on access control, data protection, system security, and incident preparedness.

---

## 3. Asset Identification
Key assets identified include:
- User accounts and credentials  
- Company laptops and endpoints  
- Email systems and communications  
- Internal documents and sensitive business data  
- Network infrastructure (routers, Wi-Fi)

---

## 4. Risk Assessment

### Risk 1: Weak Access Controls
Users may have excessive permissions or retain access after role changes, increasing the risk of unauthorised access and segregation of duties conflicts.

**Impact:** High  
**Likelihood:** Medium  

---

### Risk 2: Lack of Multi-Factor Authentication (MFA)
Accounts protected only by passwords are vulnerable to compromise.

**Impact:** High  
**Likelihood:** High  

---

### Risk 3: Unsecured Endpoints
Devices may not be properly patched or protected with antivirus software.

**Impact:** Medium  
**Likelihood:** Medium  

---

### Risk 4: Phishing and Social Engineering
Employees may not be trained to recognise phishing attempts.

**Impact:** High  
**Likelihood:** High  

---

## 5. Control Recommendations

- Implement Multi-Factor Authentication (MFA) for all users  
- Enforce least privilege access and remove shared accounts  
- Apply regular patching and endpoint protection  
- Provide basic security awareness training  
- Establish password policies (complexity + rotation)

---

## 6. Risk Summary

| Risk                          | Impact | Likelihood | Rating |
|------------------------------|--------|------------|--------|
| Weak Access Controls         | High   | Medium     | High   |
| No MFA                       | High   | High       | Critical |
| Unsecured Endpoints          | Medium | Medium     | Medium |
| Phishing Risk                | High   | High       | Critical |

---

## 7. Conclusion
The organisation faces several common but significant security risks, particularly in access control and user authentication.

These risks could result in operational disruption, data loss, or reputational damage if not addressed.

By implementing basic security controls such as MFA, access restrictions, and user awareness training, the organisation can significantly reduce its risk exposure and improve its overall security posture.

---

## 8. Framework Alignment
This assessment is broadly aligned with:
- NIST Cybersecurity Framework (Identify, Protect)
- ISO 27001 principles (access control, asset management, risk treatment)
