# Day 6 – Advanced Log Analysis & Event Interpretation

## Overview
This repository contains my learning from Day 6 of the SOC Internship Program, focusing on advanced log analysis, event interpretation, and identifying attack patterns in real-world SOC environments.

---

## Objective
- Understand key log fields used in security analysis  
- Learn important Windows Security Event IDs  
- Detect attack patterns from logs  
- Perform structured investigation  
- Map activities to SOC analyst roles (L1, L2, L3)  

---

## Key Log Fields
- **Timestamp** – Time of the event  
- **Source IP** – Origin of the activity  
- **Destination/User** – Target account or system  
- **Event Type** – Success / Failure / Action  
- **Process/Service** – Service involved (SSH, HTTP, etc.)  

---

## Important Windows Event IDs
- **4624** – Successful login  
- **4625** – Failed login attempt  
- **4672** – Admin privileges assigned  
- **4688** – Process creation  

---

## Attack Pattern Detection
- Multiple failed logins → Brute force attack  
- Unusual IP login → Suspicious access  
- Success after failures → Account compromise  
- Unknown process → Possible malware  

---

## Example Log Analysis
```
Apr 10 10:17:45 Failed password for admin from 185.12.45.10  
Apr 10 10:18:02 Failed password for admin from 185.12.45.10  
Apr 10 10:18:15 Failed password for admin from 185.12.45.10  
Apr 10 10:19:10 Accepted password for admin from 185.12.45.10  
```

### Analysis
- Repeated failed attempts from same IP  
- Targeting admin account  
- Successful login after failures  

**Conclusion:** Brute Force Attack leading to account compromise  

---

## Analysis Approach
1. Identify repeated failures  
2. Check source IP  
3. Verify login success  
4. Determine attack type  
5. Assess risk  

---

## SOC Workflow Mapping
- **L1 Analyst** – Detects suspicious activity  
- **L2 Analyst** – Investigates and responds (block IP, reset password)  
- **L3 Analyst** – Creates detection rules and improves security  

---

## Prevention Techniques
- Enable Multi-Factor Authentication (MFA)  
- Implement Account Lockout Policy  

---

## Conclusion
This session helped me understand how SOC analysts use log data to detect threats, analyze attacks, and respond effectively. It strengthened my skills in identifying patterns and performing structured investigations.

---

## Author
Adithya Raj K R  
