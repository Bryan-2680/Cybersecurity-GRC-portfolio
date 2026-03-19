# Log Analysis – Suspicious Activity Investigation

## 1. Objective
The objective of this project is to analyse system log data to identify potentially suspicious activity using basic query techniques.

The focus is on understanding how monitoring and data analysis can support early detection of security issues.

This aligns with real-world scenarios where system logs are used to support incident detection and investigation.

---

## 2. Scenario
A dataset of system activity logs is available, containing information such as user IDs, login times, IP addresses, and actions performed.

The goal is to identify unusual or potentially risky behaviour.

---

## 3. Analysis Approach
The analysis focuses on identifying patterns that may indicate suspicious activity, including:

- Multiple failed login attempts  
- Logins from unusual locations  
- Activity outside normal working hours  
- Repeated access to sensitive resources  

---

## 4. Example Queries

### Failed Login Attempts
```sql
SELECT user_id, COUNT(*) AS failed_attempts
FROM login_logs
WHERE status = 'FAILED'
GROUP BY user_id
ORDER BY failed_attempts DESC;

## 5. Key Findings

Certain users show repeated failed login attempts, which may indicate attempted credential compromise or brute force activity.
Activity outside normal working hours could indicate compromised accounts or unauthorised access
Frequent access to sensitive data may indicate excessive permissions or potential misuse

6. Control Recommendations

- Implement account lockout policies after repeated failed logins
- Monitor and alert on unusual login patterns
- Restrict and monitor access to sensitive data
- Implement logging and centralised monitoring solutions
- Conduct regular reviews of user activity

7. Conclusion

Log analysis is a key component of effective security monitoring.

By identifying unusual patterns and behaviours, organisations can detect potential threats early and take appropriate action to reduce risk.
