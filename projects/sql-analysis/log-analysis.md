# Security Monitoring Analysis – Suspicious Activity Investigation

## 1. Objective
The objective of this project is to analyse system log data to identify potentially suspicious activity using basic query techniques.

The focus is on understanding how monitoring and data analysis can support early detection of security issues.

This aligns with real-world scenarios where system logs are used to support incident detection and investigation.

---

## 2. Scenario
A dataset of system activity logs is available from a business environment, containing information such as user IDs, login times, IP addresses, and actions performed.

The purpose of the analysis is to identify abnormal behaviour that may indicate unauthorised access, weak authentication controls, or potential misuse of sensitive resources.

---

## 3. Analysis Approach
The analysis follows a risk-based approach focused on identifying activity patterns that could indicate suspicious behaviour or control weaknesses.

Key indicators reviewed include:
- Multiple failed login attempts  
- Logins from unusual locations  
- Activity outside normal working hours  
- Repeated access to sensitive resources

These indicators were selected because they may signal attempted account compromise, inappropriate access, or insufficient monitoring controls.

---

## 4. Example Queries

### Failed Login Attempts
```sql
SELECT user_id, COUNT(*) AS failed_attempts
FROM login_logs
WHERE status = 'FAILED'
GROUP BY user_id
ORDER BY failed_attempts DESC;
```

### Logins Outside Business Hours
```sql
SELECT user_id, login_time
FROM login_logs
WHERE HOUR(login_time) < 6 OR HOUR(login_time) > 20;
```

### Access to Sensitive Resources
```sql
SELECT user_id, resource, COUNT(*) AS access_count
FROM access_logs
WHERE resource = 'sensitive_data'
GROUP BY user_id, resource
ORDER BY access_count DESC;
```

### Repeated Access from the Same IP Address
```sql
SELECT ip_address, COUNT(*) AS activity_count
FROM login_logs
GROUP BY ip_address
ORDER BY activity_count DESC;
```

---

## 5. Key Findings
- Repeated failed login attempts may indicate attempted credential compromise or brute force activity  
- Logins outside normal working hours may indicate compromised accounts or unauthorised access  
- Frequent access to sensitive data may indicate excessive permissions, poor access control, or potential misuse  
- Concentrated activity from specific IP addresses may warrant further review to determine whether access is expected or anomalous  
  
These findings highlight the importance of strong authentication controls, effective monitoring, and regular access reviews.

---

## 6. Control Recommendations
- Implement account lockout policies after repeated failed logins  
- Monitor and alert on unusual login patterns and access anomalies  
- Restrict and monitor access to sensitive data  
- Implement centralised logging and monitoring solutions  
- Conduct regular reviews of user activity and access permissions  
- Define thresholds for abnormal behaviour and establish escalation procedures for investigation  

---

## 7. Conclusion
Security monitoring is a key component of effective cybersecurity risk management.

By identifying unusual patterns and behaviours in system logs, organisations can detect potential threats early, investigate suspicious activity, and take action to reduce operational and security risk.

This project demonstrates how structured analysis of log data supports both incident detection and ongoing control improvement.
