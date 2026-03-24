# Access Control Assessment – Least Privilege and Access Misuse

This assessment examines how weaknesses in access governance and information sharing controls can increase the risk of unauthorised activity, fraud, and data exposure.

## 1. Objective
The objective of this assessment is to evaluate access control risks within a role-based business environment, identify weaknesses related to excessive permissions, segregation of duties, access governance, and inappropriate data sharing, and recommend practical controls to reduce operational, compliance, and information security risk.

---

## 2. Scenario
The environment consists of a business-critical enterprise system supporting operational and transactional processes. 

Users are assigned access based on business need, but over time may accumulate unnecessary permissions due to role changes, temporary access, poor offboarding, or lack of regular access reviews.

The assessment also considers the risk of sensitive information being exposed through inappropriate sharing practices where least privilege is not effectively enforced.

---

## 3. Assessment Approach

This assessment follows a risk-based approach focused on user access, role design, control effectiveness, and the handling of sensitive information.

The review considers how excessive permissions, conflicting access rights, weak lifecycle management, and unrestricted sharing can increase the likelihood of unauthorised activity, fraud, or data exposure.

Risks were evaluated based on their potential business impact and likelihood of occurrence.

---

## 4. Key Risks Identified

### Risk 1: Excessive Permissions
Users may have access beyond what is required for their role, increasing the risk of unauthorised actions, accidental changes, or misuse of sensitive information.

This is particularly relevant in systems supporting financial, operational, or customer-related processes.

**Impact:** High  
**Likelihood:** Medium  

---

### Risk 2: Segregation of Duties Conflicts
A single user may have access to perform conflicting functions, such as creating and approving transactions, increasing the risk of fraud, error, or control bypass.

This is particularly significant in environments where financial or approval-based processes are involved.

**Impact:** High  
**Likelihood:** Medium  

---

### Risk 3: Inadequate Access Reviews and Offboarding
Access may not be reviewed regularly, and permissions may remain active after role changes or when access is no longer required.

This increases the risk of dormant, excessive, or inappropriate access persisting over time.

**Impact:** High  
**Likelihood:** High  

---

### Risk 4: Inappropriate Sharing of Sensitive Information
Sensitive documents or folders may be shared too broadly due to weak access restrictions or failure to remove temporary access.

This creates a risk of internal information being exposed to unauthorised parties, either accidentally or through poor handling practices.

**Impact:** High  
**Likelihood:** Medium  

---

## 5. Business Impact
Weak access control practices can result in:

- Unauthorised transactions or inappropriate system activity  
- Fraud, error, or control bypass  
- Exposure of sensitive internal or customer-related information  
- Reduced accountability and auditability  
- Compliance and regulatory risk  
- Reputational damage and loss of stakeholder trust  

---

## 6. Control Recommendations
To reduce the identified risks, the following controls are recommended:

- Enforce least privilege access principles across systems and shared resources  
- Implement regular user access reviews and periodic recertification by business or system owners  
- Define and enforce segregation of duties rules for sensitive or approval-based activities  
- Strengthen joiner, mover, leaver processes to ensure access is removed or updated promptly  
- Restrict the sharing of sensitive folders and documents to approved users only  
- Implement time-bound access for temporary permissions where appropriate  
- Maintain audit logs for user access, file sharing, and privileged activities  
- Implement automated controls to detect and prevent segregation of duties conflicts  

---

## 7. Framework Alignment
This assessment is broadly aligned with:

- Least privilege principles  
- Role-based access control (RBAC) good practice  
- NIST SP 800-53 AC-6 (Least Privilege)  
- Governance and control principles supporting accountability and appropriate access management  

---

## 8. Conclusion
Access control is a critical part of an organisation’s security and governance framework.

Weaknesses in access design, review processes, and information sharing controls can lead to unauthorised activity, fraud, or data exposure if not properly managed.

By strengthening least privilege, improving access governance, and restricting unnecessary sharing, organisations can significantly reduce operational, compliance, and information security risk.
