# Security Audit Report – Small Enterprise Environment

## 1. Objective
The objective of this audit is to assess the security posture of a small enterprise IT environment, identify key risks, and recommend practical controls to reduce business and operational risk, aligned with industry best practices.

---

## 2. Scope
This audit considers a small organisation with the following environment:
- 25 employees
- Cloud-based email system (e.g. Microsoft 365)
- Shared file storage
- Basic internal network
- No dedicated security team

The assessment focuses on access control, data protection, system security, and incident preparedness.

The audit is informed by recognised frameworks such as the NIST Cybersecurity Framework and ISO 27001 principles.

---

## 3. Asset Identification
Key assets identified include:
- User accounts and credentials  
- Company laptops and endpoints  
- Email systems and communications  
- Internal documents and sensitive business data  
- Network infrastructure (routers, Wi-Fi)
  
---

## 4. Audit Approach
The audit was conducted using a risk-based approach, focusing on identifying key assets, assessing potential threats and vulnerabilities, and evaluating the effectiveness of existing or expected controls.

Risks were prioritised based on potential business impact and likelihood of occurrence.

---

## 5. Risk Assessment

### Risk 1: Weak Access Controls
Users may have excessive permissions or retain access after role changes, increasing the risk of unauthorised access and segregation of duties conflicts.

**Impact:** High  
**Likelihood:** Medium  

---

### Risk 2: Lack of Multi-Factor Authentication (MFA)
Accounts protected only by passwords are vulnerable to compromise through phishing, credential reuse, or brute force attacks

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
## 6. Risk Rating Method

Risk ratings are determined based on a combination of impact and likelihood:

- **Impact**: The potential business consequence if the risk materialises (e.g. data loss, operational disruption)
- **Likelihood**: The probability of the risk occurring based on the current control environment

Risk levels are classified as Low, Medium, High, or Critical.

---

## 7. Risk Summary & Prioritisation

| Risk                          | Impact | Likelihood | Rating |
|------------------------------|--------|------------|--------|
| Weak Access Controls         | High   | Medium     | High   |
| No MFA                       | High   | High       | Critical |
| Unsecured Endpoints          | Medium | Medium     | Medium |
| Phishing Risk                | High   | High       | Critical |

---

## 8. Control Recommendations

- Implement Multi-Factor Authentication (MFA) for all users  
- Enforce least privilege access and remove shared accounts  
- Apply regular patching and endpoint protection  
- Provide regular security awareness training, particularly focused on phishing and credential security  
- Establish password policies (complexity + rotation)
- Define clear ownership and accountability for security controls and risk management activities
- Implement basic logging and monitoring to detect suspicious activity

---

## 9. Conclusion
The organisation faces several significant security risks, particularly in access control, authentication, and user awareness.

These risks could result in operational disruption, data loss, or reputational damage if not addressed.

By implementing basic security controls such as MFA, access restrictions, and user awareness training, the organisation can significantly reduce its risk exposure and improve its overall security posture.

This assessment demonstrates a structured, risk-based approach to identifying security weaknesses and recommending practical controls in a small enterprise environment.

---

## 10. Framework Alignment
This assessment is broadly aligned with:
- NIST Cybersecurity Framework (Identify, Protect)
- ISO 27001 principles (access control, asset management, risk treatment)
