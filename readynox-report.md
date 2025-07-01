### **Cybersecurity Internship Report**  

---

### **1. Introduction**  
This report documents my internship tasks at Redynox, focused on network security, web application security, and professional branding. Objectives included:  
- Implementing foundational network defenses.  
- Identifying and exploiting web vulnerabilities.  
- Enhancing professional visibility via LinkedIn.  

---

### **2. Task Overview**  
#### **2.1 Task 1: Introduction to Network Security Basics**  
**Objective:**  
Understand network threats and implement basic security measures.  

**Tools & Methods:**  
- **Tools:** Windows Defender Firewall, Wireshark, home router.  
- **Methods:** Firewall configuration, traffic analysis, encryption setup.  

**Steps Taken (Followed PDF Guidelines Exactly):**  
1. **Learned Network Security Concepts:**  
   - Researched and summarized threats:  
     - **Viruses/Worms:** Self-replicating malware.  
     - **Trojans:** Disguised malicious software.  
     - **Phishing:** Social engineering attacks.  
   - Studied firewalls, encryption (AES), and secure configurations.  

2. **Implemented Basic Security Measures:**  
   - Configured a home lab network (router + 2 devices).  
   - Enabled **Windows Defender Firewall** with rules blocking unsolicited inbound traffic.  
   - Changed router’s default admin password to a complex phrase.  
   - Enforced **WPA3 encryption** on the Wi-Fi network.  

3. **Monitored Network Traffic:**  
   - Captured 1 hour of traffic using **Wireshark**.  
   - Identified traffic types:  
     - **HTTP:** Unencrypted web requests.  
     - **DNS:** Domain resolution queries.  
   - Detected suspicious activity: Repetitive DNS requests to unknown domains (potential beaconing).  

4. **Documented Findings:**  
   - Included:  
   
     
5. **Reflected on Security Best Practices:**  
   - **Additional Measures for Larger Networks:**  
     - Implement IDS/IPS, network segmentation, and VPNs.  
   - **Education Approach:**  
     *"I’d conduct workshops highlighting real-world phishing examples and teach password hygiene to help non-technical users recognize risks."*  

**Challenges & Solutions:**  
- **Challenge:** Wireshark’s data overload.  
  **Solution:** Used filters (`dns && ip.dst==8.8.8.8`) to isolate key traffic.  
- **Challenge:** Router compatibility with WPA3.  
  **Solution:** Updated firmware to enable modern encryption.  

**Results & Outcomes:**  
- Secured network against basic threats.  
- Identified & documented DNS anomalies.  

---

#### **2.2 Task 2: Introduction to Web Application Security**  
**Objective:**  
Identify and exploit web application vulnerabilities.  

**Tools & Methods:**  
- **Tools:** OWASP ZAP, WebGoat.  
- **Methods:** Automated scanning, manual exploitation.  

**Steps Taken (Followed PDF Guidelines Exactly):**  
1. **Setup:**  
   - Installed **WebGoat** locally (`http://localhost:8080/WebGoat`).  

2. **Performed Vulnerability Analysis:**  
   - Scanned WebGoat with **OWASP ZAP**, discovering:  
     - **SQL Injection** in login form.  
     - **Reflected XSS** in search field.  
     - **CSRF** in profile update feature.  

3. **Explored Vulnerabilities:**  
   - **SQLi Exploit:** Used `' OR 1=1--` to bypass authentication.  
   - **XSS Exploit:** Injected `<script>alert("XSS")</script>` to hijack sessions.  
   - **CSRF Exploit:** Crafted malicious form forcing password reset.  

4. **Reported Findings:**  
   - **Documentation per Vulnerability:**  
     | Vulnerability | How Discovered         | Risk                          | Mitigation            |  
     |---------------|------------------------|-------------------------------|-----------------------|  
     | SQLi          | ZAP scan + manual test | Data theft                    | Parameterized queries |  
     | XSS           | Manual input testing   | Session hijacking             | Input sanitization    |  
     | CSRF          | ZAP alert verification | Unauthorized actions          | Anti-CSRF tokens      |  
   - Included screenshots of ZAP scan results and successful exploits.  

**Challenges & Solutions:**  
- **Challenge:** WebGoat setup errors.  
  **Solution:** Ran with Java 11 and adjusted permissions.  
- **Challenge:** ZAP false positives.  
  **Solution:** Manually validated each vulnerability.  

**Results & Outcomes:**  
- Confirmed 3 critical vulnerabilities with proof-of-concept exploits.  
- Recommended mitigations aligned with OWASP Top 10.  

---
**Dinesh Kumar**  
Cybersecurity Intern, Redynox  
*Date: 01 July 2025*
