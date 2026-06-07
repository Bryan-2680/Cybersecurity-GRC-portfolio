## Security Assessment Report – Small Enterprise Environment

### 1. Objective
To assess the security posture of a small enterprise IT environment, identify key risks, and recommend practical controls to reduce business and operational risk, aligned with recognised industry frameworks.

Note: This is a demonstrative scenario built to apply a structured, risk-based assessment method using NIST CSF and ISO 27001 principles. It is anonymised and
illustrative — a security assessment (posture review), not a formal compliance audit of a real organisation.

---

### 2. Scope
A small organisation with the following environment:
- 25 employees
- Cloud-based email system (e.g. Microsoft 365)
- Shared file storage
- Basic internal network
- No dedicated security team

The assessment focuses on access control, data protection, system security, and incident preparedness, informed by the NIST Cybersecurity Framework and ISO/IEC 27001 principles.

---

### 3. Asset Identification
Key assets identified include:
- User accounts and credentials  
- Company laptops and endpoints  
- Email systems and communications  
- Internal documents and sensitive business data  
- Network infrastructure (routers, Wi-Fi)
  
---

### 4. Assessment Approach

A risk-based approach: identifying key assets, assessing potential threats and vulnerabilities, and evaluating the effectiveness of existing or expected controls.
Risks were prioritised on a qualitative likelihood × impact basis.

---

### 5. Risk Assessment

Each risk below includes the reasoning behind its rating, not just the score.

#### Risk 1: Weak Access Controls
Users may have excessive permissions or retain access after role changes, increasing the risk of unauthorised access and segregation of duties conflicts.

**Impact:** High  
**Likelihood:** Medium  

Rationale: impact is high because excessive access in business-critical systems enables unauthorised or fraudulent activity; likelihood is medium because such issues accrue gradually through role changes rather than constantly.

#### Risk 2: Lack of Multi-Factor Authentication (MFA)
Accounts protected only by passwords are vulnerable to compromise through phishing, credential reuse, or brute force attacks. 

**Impact:** High  
**Likelihood:** High  

Rationale: likelihood is high because password-only accounts are a primary attack target and there is no security team to detect compromise; impact is high because a single compromised account can expose email and shared data. The combination makes this the top priority.

#### Risk 3: Unsecured Endpoints
Devices may not be properly patched or protected with antivirus software.

**Impact:** Medium  
**Likelihood:** Medium  

Rationale: exploitation usually requires another trigger (e.g. a malicious download), and impact is typically contained to the affected device, so both factors are moderate.

#### Risk 4: Phishing and Social Engineering
Employees may not be trained to recognise phishing attempts.

**Impact:** High  
**Likelihood:** High  

Rationale: likelihood is high because phishing is the most common initial attack vector and untrained users in a no-security-team environment are especially exposed; impact is high because a successful phish often leads directly to account compromise (linking back to Risk 2). 

---

### 6. Risk Rating Method

Ratings combine impact and likelihood:

- **Impact**: The potential business consequence if the risk materialises (e.g. data loss, operational disruption). 
- **Likelihood**: The probability occurrance based on the given control environment. 

Risk levels are classified as Low, Medium, High, or Critical.

---

### 7. Risk Summary & Prioritisation

| Risk                          | Impact | Likelihood | Rating |
|------------------------------|--------|------------|--------|
| Phishing Risk                | High   | High       | Critical |
| No MFA                       | High   | High       | Critical |
| Weak Access Controls         | High   | Medium     | High   |
| Unsecured Endpoints          | Medium | Medium     | Medium |

Ordered by priority — the two Critical risks (MFA and phishing) are closely linked and should be addressed first.

---

### 8. Control Recommendations

- Implement Multi-Factor Authentication (MFA) for all users  
- Enforce least privilege access and remove shared accounts  
- Apply regular patching and endpoint protection  
- Provide regular security awareness training, particularly focused on phishing and credential security  
- Establish password policies (complexity + rotation)
- Define clear ownership and accountability for security controls and risk management activities
- Implement basic logging and monitoring to detect suspicious activity

---

### 9.  Framework Alignment
This assessment is broadly aligned with:

- NIST Cybersecurity Framework — primarily Identify (asset identification, risk assessment) and Protect (access control, MFA, training), with the logging/monitoring
recommendation touching Detect and the incident-preparedness scope touching Respond. (The full CSF functions are Govern, Identify, Protect, Detect, Respond, Recover.)
- ISO/IEC 27001 principles — access control, asset management, and risk treatment.

---

### 10.Conclusion

The organisation faces several significant security risks, particularly in access control, authentication, and user awareness - which could lead to operational disruption, data loss, or reputational damage if not addressed.

Prioritising the two Critical risks (MFA and phishing awareness), followed by access control and endpoint hardening, would significantly reduce the organisation's exposurefor relatively low cost. 

This assessment demonstrates a structured, risk-based approach to identifying weaknesses and recommending proportionate, practical controls in a small enterprise environment.
