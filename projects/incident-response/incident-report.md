# Incident Response Report – Integration Failure Scenario

This report presents an incident response case study involving a system integration failure, focusing on detection, structured investigation, root cause analysis, and preventative controls. The report follows the NIST SP 800-61 incident-response lifecycle: Preparation; Detection & Analysis, Containment, Eradication & Recovery, and Post-Incident Activity applied to a realistic enterprise integration scenario. 

Note: This is a demonstrative scenario based on the types of EDI / system integration failures common in enterprise SAP environments. It is anonymised and
intended to show the application of a structured incident-response method, not to describe a specific real-world event.

## 1. Incident Overview
An issue was identified where purchase order (PO) messages failed to be successfully transmitted between an internal system and an external vendor, resulting in delays in order processing.

The incident affected communication between internal systems and external vendors, disrupting normal PO and invoice processing and delaying downstream fulfilment

**Severity:** Medium (operational impact; no data loss identified)

---

## 2. Detection & Analysis

### 2.1 Detection

The incident was initially identified when a vendor reported that they had not received a purchase order they were expecting. This external report — rather than an
internal alert — was the first signal, which itself became a key lesson. 

Follow-up checks confirmed the issue: failed transactions and missing functional acknowledgements were identified, verifying that messages were not being processed
correctly.

### 2.2. Investigation & Root Cause Analysis
Investigation followed a structured elimination process to isolate the failure point along the message path, rather than assuming a cause.

- Message generation - Confirmed the purchase order messages were being created correctly in the source system, ruling out an upstream data or generation error.

- Outbound transmission - Checked that messages were leaving the source system and reaching the middleware/integration layer, to distinguish an internal failure from a transmission/connectivity issue.

- Connectivity and certificates - Verified the connection and certificate validity to the vendor endpoint, ruling out an expired certificate or network failure as the cause.

- Acknowledgements - Identified missing functional acknowledgements, confirming messages were not being successfully processed at the destination rather than simply lost in transit.

- Configuration and validation - Traced the failure to an internal configuration issue affecting message processing and validation, which caused transactions to fail validation and not complete.

This step-by-step approach eliminated potential issues and isolated the root cause to a configuration error, rather than a connectivity, certificate, or vendor-side issue — ensuring the correct fix was applied the first time rather than through trial and error.

---

## 3. Timeline
- Vendor reports a missing/expected purchase order
- Failed transactions and missing acknowledgements confirmed
- Structured investigation initiated along the message path
- Root cause isolated to an internal configuration issue
- Fix implemented and affected transactions reprocessed
- System monitored to confirm restoration of normal operations

---

## 4. Impact Assessment
- Delayed order processing  
- Potential disruption to supply chain operations  
- Risk of incomplete or duplicate transactions  
- Increased manual intervention required
- Potential financial and reputational impact due to delayed or incorrect order fulfilment

The incident had operational impact and required timely resolution to prevent further disruption.

---

## 5. Containment, Eradication & Recovery

- Containment - identified the scope of affected transactions to prevent further
failed messages from compounding the backlog.

- Eradication — corrected the underlying configuration issue affecting message
processing and validation.

- Recovery — reprocessed the affected transactions and monitored the system to
confirm restoration of normal operations and successful acknowledgements.
 
---

## 6. Post-Incident Activity

### 6.1 Lessons Learned

- Detection relied on an external vendor report rather than internal monitoring — highlighting the need for proactive alerting for earlier detection.
- Limited real-time visibility of transaction failures slowed initial detection.
- A structured, repeatable investigation method (elimination along the message path) shortened root-cause analysis and should be standardised.
- Configuration management and validation controls are critical to preventing recurrence.

### 6.2. Preventative Controls

Based on the incident, the following control improvements are recommended:

- Implement automated alerting for failed transactions  
- Improve logging and monitoring capabilities   
- Implement validation checks for system configurations
- Establish clear escalation procedures for incident handling
- Define ownership and accountability for incident response and system configuration management

---

## 7. Conclusion
This incident highlights the importance of effective monitoring, structured investigation, and control design in maintaining system reliability. Mapping the
response to the NIST incident-response lifecycle ensured each phase — from detection through to post-incident improvement — was addressed deliberately rather than
reactively.

Addressing the identified control gaps, particularly proactive monitoring and configuration validation, would reduce the likelihood of recurrence and strengthen
overall operational resilience.
