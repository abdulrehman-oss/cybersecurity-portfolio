# SOC-Projects

# Incident Response Report

## SSH Brute-Force Detection & Automated Mitigation Using Wazuh

### Executive Summary

This report documents the detection, investigation, and mitigation of an SSH brute-force attack against a Linux system. The attack was simulated using Hydra/Ncrack from an attacker machine and monitored through Wazuh SIEM. Multiple failed authentication attempts were detected, analyzed, and correlated to identify malicious activity. Automated mitigation was then applied using Linux firewall rules (iptables) to block the attack source and prevent further unauthorized access.

---

## 1. Attack Overview

### Objective

To simulate an SSH brute-force attack against a Linux target and demonstrate how Wazuh can detect, investigate, and support mitigation of the attack.

### Environment

| Component          | Description                |
| ------------------ | -------------------------- |
| Attacker Machine   | Kali Linux                 |
| Target Machine     | Metasploitable 2           |
| Detection Platform | Wazuh SIEM                 |
| Attack Type        | SSH Brute Force            |
| Mitigation         | IP Blocking using iptables |

---

## 2. Attack Source

### Description

An SSH brute-force attack was launched from the Kali Linux machine against the target server using Ncrack. The attacker attempted multiple username/password combinations to gain unauthorized access.

### Screenshot 1 Caption

**Figure 1: SSH brute-force attack launched from Kali Linux using Ncrack against the target SSH service.**

*(Place Screenshot 1 here)*

### Analysis

The attack generated repeated authentication failures on the target host. These failed login attempts were recorded in system authentication logs and subsequently collected by Wazuh for analysis.

---

## 3. Detection and Timeline

### Description

Wazuh detected multiple failed SSH authentication attempts and generated security alerts. The alerts were correlated over time, indicating a brute-force attack pattern.

### Screenshot 2 Caption

**Figure 2: Wazuh dashboard displaying SSH brute-force related alerts and event timeline.**

*(Place Screenshot 2 here)*

### Timeline of Events

| Time | Event                                             |
| ---- | ------------------------------------------------- |
| T0   | Attacker initiates SSH brute-force attack         |
| T1   | Multiple failed authentication attempts recorded  |
| T2   | Wazuh generates SSH authentication failure alerts |
| T3   | Security investigation initiated                  |
| T4   | Source IP identified                              |
| T5   | Firewall mitigation applied                       |
| T6   | Attack traffic blocked successfully               |

---

## 4. Indicators of Compromise (IOCs)

### Description

Investigation of authentication logs revealed repeated failed login attempts originating from a single source system. Such behavior is a common indicator of brute-force activity.

### Screenshot 3 Caption

**Figure 3: Authentication logs showing multiple failed SSH login attempts and associated security events.**

*(Place Screenshot 3 here)*

### Identified IOCs

* Multiple failed SSH authentication attempts.
* Repeated login requests within a short period.
* Suspicious source IP generating authentication failures.
* Increased authentication-related log volume.
* Wazuh alerts indicating brute-force behavior.

### Impact Assessment

Although no successful compromise occurred, the attack demonstrated an active attempt to gain unauthorized access to the target system. Without proper controls, such attacks could eventually result in credential compromise and system intrusion.

---

## 5. Mitigation Actions

### Description

After identifying the malicious source, firewall rules were implemented using iptables to block the attacking IP address and prevent further connection attempts.

### Screenshot 4 Caption

**Figure 4: Firewall configuration showing the malicious source blocked using iptables rules.**

*(Place Screenshot 4 here)*

### Mitigation Steps

1. Identified attack source through Wazuh alerts.
2. Verified attack activity using authentication logs.
3. Implemented firewall rule to block attacker IP.
4. Confirmed traffic was successfully denied.
5. Continued monitoring for additional attack attempts.

### Verification

Post-mitigation monitoring showed no further successful connection attempts from the identified source. Firewall rules effectively prevented continued brute-force activity.

---

## 6. Lessons Learned

* Wazuh provides effective detection of SSH brute-force attacks.
* Log correlation significantly improves incident visibility.
* Rapid identification of attack sources enables timely response.
* Firewall-based blocking is an effective immediate containment strategy.
* Continuous monitoring is essential for identifying recurring attack attempts.

---

## 7. Conclusion

The SSH brute-force attack was successfully detected through Wazuh SIEM and investigated using authentication logs. Indicators of compromise were identified, and the malicious source was blocked using firewall controls. The exercise demonstrates the effectiveness of SIEM-based monitoring and incident response procedures in detecting and mitigating credential-based attacks.

---

### Skills Demonstrated

* Security Monitoring
* SIEM Analysis (Wazuh)
* Incident Investigation
* Log Analysis
* Threat Detection
* SSH Security
* Linux Administration
* Firewall Management (iptables)
* Incident Response
* Documentation & Reporting
