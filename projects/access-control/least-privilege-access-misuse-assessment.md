## Access Control Assessment – Least Privilege and Access Misuse

This assessment examines how weaknesses in access governance and information sharing controls can increase the risk of unauthorised activity, fraud, and data exposure.

Note: This is a demonstrative scenario based on common access-control risks in role-based enterprise systems. It is anonymised and intended to show the application
of a structured, risk-based access assessment, not to describe a specific real-world environment.

### 1. Objective
The objective of this assessment is to evaluate access control risks within a role-based business environment, identify weaknesses related to excessive permissions, segregation of duties, access governance, and inappropriate data sharing, and recommend practical controls to reduce operational, compliance, and information security risk.

---

### 2. Scenario
The environment is a business-critical enterprise system supporting operational and transactional processes. 

Users are assigned access based on business need, but over time may accumulate unnecessary permissions due to role changes, temporary access, weak offboarding, or lack of regular access reviews.

The assessment also considers the risk of sensitive information being exposed through inappropriate sharing where least privilege is not effectively enforced.

---

### 3. Assessment Approach

This assessment follows a qualitative, risk-based approach, with each risk scored on a likelihood × impact basis to support prioritisation. The review focuses on user access, role design, control effectiveness, and the handling of sensitive information —considering how excessive permissions, conflicting access rights, weak lifecycle management, and unrestricted sharing increase the likelihood of unauthorised activity,
fraud, or data exposure.

---

### 4. Key Risks Identified

#### Risk 1: Excessive Permissions
Users may hold access beyond what their role requires, increasing the risk of unauthorised actions, accidental changes, or misuse of sensitive information —
particularly in systems supporting financial, operational, or customer processes

**Impact:** High  
**Likelihood:** Medium  

#### Risk 2: Segregation of Duties Conflicts
A single user may be able to perform conflicting functions, such as creating and approving transactions, increasing the risk of fraud, error, or control bypass —
especially significant in approval-based financial processes

**Impact:** High  
**Likelihood:** Medium  

#### Risk 3: Inadequate Access Reviews and Offboarding
Access may not be reviewed regularly, and permissions may persist after role changes or once no longer required, leaving dormant, excessive, or inappropriate access in place.

**Impact:** High  
**Likelihood:** High  

#### Risk 4: Inappropriate Sharing of Sensitive Information
Sensitive documents or folders may be shared too broadly due to weak restrictions orfailure to remove temporary access, exposing internal information to unauthorised parties accidentally or through poor handling.

**Impact:** High  
**Likelihood:** Medium  

---

### 5. Example – Identifying a Segregation of Duties Conflict
To illustrate the assessment in practice, consider a representative case:

A user moves from the Procurement team to the Finance team. Their new Finance role grants invoice/payment approval rights, but their previous purchase-order
creation rights were never removed during the move.

The user can now both create a purchase order and approve the corresponding payment creating segregation of duties (SoD) conflict. A single individual controlling both sides of the transaction creates a fraud and error exposure, because no independent check sits between initiation and approval.

This single case demonstrates two of the risks below at once: an SoD conflict (Risk 2) arising directly from weak mover/leaver access management (Risk 3). The remediation — removing the redundant PO-creation right on role change and adding an SoD rule to detect create-plus-approve combinations — maps directly to the recommended controls inSection 7.

---


### 6. Business Impact

Weak access control practices can result in:
- Unauthorised transactions or inappropriate system activity  
- Fraud, error, or control bypass  
- Exposure of sensitive internal or customer-related information  
- Reduced accountability and auditability  
- Compliance and regulatory risk  
- Reputational damage and loss of stakeholder trust  

---

### 7. Control Recommendations

- Enforce least privilege access principles across systems and shared resources  
- Implement regular user access reviews and periodic recertification by business or system owners  
- Define and enforce segregation of duties rules for sensitive or approval-based activities  
- Strengthen joiner/mover/leaver processes to ensure access is removed or updated promptly  
- Restrict the sharing of sensitive folders and documents to approved users only  
- Implement time-bound access for temporary permissions. 
- Maintain audit logs for user access, file sharing, and privileged activities  
- Implement automated controls to detect and prevent segregation of duties conflicts  

---

### 8. Framework Alignment
This assessment is broadly aligned with:

- Least privilege principles ans role-based access control (RBAC) good practice  
- NIST SP 800-53 AC-6 (Least Privilege)  
- ISO/IEC 27001 Annex A access-control objectives (access management, user access provisioning, and review of user access rights  

---

## 8. Conclusion
Access control is a critical part of an organisation’s security and governance framework. Weaknesses in access design, review processes, and information sharing controls can lead to unauthorised activity, fraud, or data exposure if not properly managed.

By enforcing least privilege, improving access governance through regular reviews and strong joiner/mover/leaver processes, and restricting unnecessary sharing,
organisations can significantly reduce operational, compliance, and information security risk.
