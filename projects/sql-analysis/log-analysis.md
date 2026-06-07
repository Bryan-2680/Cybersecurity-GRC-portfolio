## Security Monitoring Analysis – Suspicious Activity Investigation

### 1. Objective
To analyse system log data using SQL queries to identify potentially suspiciousactivity, demonstrating how monitoring and structured data analysis support the earlydetection and investigation of security issues. This maps to the Detect function of the NIST Cybersecurity Framework — establishing baselines and surfacing deviations.

Note: This is a demonstrative log-analysis exercise using illustrative sample data. It is anonymised and intended to show the use of SQL to query authentication and access logs for suspicious patterns, not to describe a real production environment or SIEM platform.

---

### 2. Scenario
A dataset of system activity logs from a business environment, containing user IDs, login times, IP addresses, status, and actions performed. The goal is to identify abnormal behaviour that may indicate unauthorised access, weak authentication controls, or misuse of sensitive resources.

---

### 3. Analysis Approach
A risk-based approach focused on identifying activity patterns that could indicate suspicious behaviour or control weaknesses. 

Detection indicators reviewed:
- Multiple failed login attempts  
- Logins from unusual locations  
- Activity outside normal working hours  
- Repeated access to sensitive resources

These were selected because they are common indicators of attempted account compromise, inappropriate access, or insufficient monitoring — and they form recognised detection use-cases in security monitoring.

---

### 4. Queries and Illustrative Findings

Each query is followed by representative sample output and an interpretation, to show not just the query but how an analyst would read the result.

#### Failed Login Attempts
```sql
SELECT user_id, COUNT(*) AS failed_attempts
FROM login_logs
WHERE status = 'FAILED'
GROUP BY user_id
ORDER BY failed_attempts DESC;
```
Explanation: groups failed logins by user and counts them, surfacing accounts with abnormal failure volumes.

Illustrative result: user_id 4172 returned 47 failed attempts within one hour, against a baseline of 2–3 for other users. This concentration is consistent with a
brute-force or credential-stuffing attempt and would warrant immediate investigation and a temporary account lock.

#### Logins Outside Business Hours
```sql
SELECT user_id, login_time
FROM login_logs
WHERE HOUR(login_time) < 6 OR HOUR(login_time) > 20;
```
Explanation: flags logins outside a 06:00–20:00 window as candidates for review.

Illustrative result: a successful login for user_id 2210 at 03:14 stood out against that user's normal 09:00–17:00 pattern — a possible compromised account or
unauthorised access requiring confirmation with the user.

#### Access to Sensitive Resources
```sql
SELECT user_id, resource, COUNT(*) AS access_count
FROM access_logs
WHERE resource = 'sensitive_data'
GROUP BY user_id, resource
ORDER BY access_count DESC;
```
Explanation: counts accesses to a sensitive resource per user to surface disproportionate access.

Illustrative result: one user accounted for a high share of sensitive-data accesses relative to peers — potentially excessive permissions, misuse, or simply a legitimate role, and therefore a candidate for an access review rather than an immediate alert.

#### Repeated Access from the Same IP Address
```sql
SELECT ip_address, COUNT(*) AS activity_count
FROM login_logs
GROUP BY ip_address
ORDER BY activity_count DESC;
```
Explanation: aggregates activity by source IP to identify concentrated or anomalous origins.

Illustrative result: a single unfamiliar IP generated a disproportionate volume of login activity, warranting a check of whether the source is an expected service/VPN or an anomalous external origin.

---

### 5. Key Findings
- High volumes of failed logins for a single account indicate likely credential compromise or brute-force activity.
- Successful logins outside normal hours may indicate compromised accounts or unauthorised access.
- Disproportionate access to sensitive data may indicate excessive permissions or misuse, and should trigger an access review.
- Concentrated activity from a single IP may be benign (VPN/service) or anomalous, and needs context before escalation.

A recurring theme: raw indicators require baselining and context before they become findings — the value is in distinguishing genuine anomalies from normal behaviour.

---

### 6. Control Recommendations
- Implement account lockout policies after repeated failed logins  
- Monitor and alert on unusual login patterns and access anomalies  
- Restrict and monitor access to sensitive data  
- Implement centralised logging and monitoring solutions  
- Conduct regular reviews of user activity and access permissions  
- Define thresholds for abnormal behaviour and establish escalation procedures for investigation  

---

### 7. Framework Alignment
This project supports the NIST Cybersecurity Framework – Detect function (anomalies and events; security continuous monitoring), and reinforces Protect through the authentication and access-control recommendations

---

### 8. Conclusion
Security monitoring is a key component of effective cybersecurity risk management. By querying log data for unusual patterns — and, importantly, interpreting those patterns against a baseline — organisations can detect potential threats early, investigate suspicious activity, and improve controls. 

This project demonstrates how structured SQL-based log analysis supports both incident detection and ongoing control improvement.
