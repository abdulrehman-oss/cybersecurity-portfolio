# 🔥 Denial of Service (DoS) Attack Simulation & Mitigation

## 📌 Project Overview

This project demonstrates how common Denial of Service (DoS) attacks can affect network services and how defensive security mechanisms can reduce their impact.

The lab was built in a controlled virtualized environment using Kali Linux as the attacker machine and Metasploitable as the victim machine. Two different attack types were simulated:

* SYN Flood Attack
* HTTP Flood Attack

After generating the attacks, mitigation techniques were implemented and tested to analyze their effectiveness.

---

## 🎯 Objectives

* Understand the fundamentals of Denial of Service attacks.
* Simulate SYN Flood and HTTP Flood attacks in a safe lab environment.
* Observe the impact of attacks on target services.
* Apply defensive mitigation techniques.
* Verify the effectiveness of implemented security controls.

---

## 🛠 Lab Environment

| Component        | Description           |
| ---------------- | --------------------- |
| Hypervisor       | VirtualBox / VMware   |
| Attacker Machine | Kali Linux            |
| Victim Machine   | Metasploitable        |
| Network Type     | Host-Only / NAT       |
| Attack Types     | SYN Flood, HTTP Flood |

---

## 🚨 Attack 1: SYN Flood

### What is a SYN Flood?

A SYN Flood attack abuses the TCP three-way handshake process by sending large numbers of SYN packets without completing the connection.

As a result:

* Half-open connections accumulate.
* Server resources become exhausted.
* Legitimate users may be unable to access services.

### Monitoring

The victim system was monitored for excessive half-open TCP connections.

Indicators observed:

* Increased SYN_RECV states
* Resource consumption
* Network congestion

---

## 🛡 SYN Flood Mitigation

Mitigation methods implemented:

* TCP SYN Cookies
* Firewall-based filtering
* Connection handling improvements

### Expected Result

* Reduction in half-open TCP connections
* Improved server stability
* Better resistance against SYN Flood traffic

---

## 🌐 Attack 2: HTTP Flood

### What is an HTTP Flood?

An HTTP Flood attack targets the application layer by overwhelming a web server with excessive HTTP requests.

Effects include:

* High CPU usage
* Increased memory consumption
* Reduced server responsiveness

---

## 🛡 HTTP Flood Mitigation

Mitigation methods implemented:

* Request rate limiting
* Firewall filtering
* Traffic control mechanisms

### Expected Result

* Controlled request volume
* Reduced server load
* Improved service availability

---

## 📊 Results

| Attack Type | Before Mitigation                    | After Mitigation                       |
| ----------- | ------------------------------------ | -------------------------------------- |
| SYN Flood   | High number of half-open connections | Reduced connection buildup             |
| HTTP Flood  | Increased server load                | Improved stability and traffic control |

---

## 🔍 Skills Demonstrated

### Cybersecurity

* Network Security
* Offensive Security Concepts
* Defensive Security Controls
* Security Monitoring
* Attack Analysis

### Tools & Technologies

* Kali Linux
* Metasploitable
* VirtualBox / VMware
* Linux Networking
* Firewall Configuration
* Traffic Monitoring

---

## 📚 Key Learning Outcomes

Through this project I gained hands-on experience in:

* Understanding DoS attack behavior
* Identifying attack indicators
* Monitoring system resources
* Implementing mitigation strategies
* Evaluating defensive security controls

---

## ⚠ Disclaimer

This project was conducted in a controlled virtual laboratory environment for educational and defensive security purposes only. No attacks were performed against public systems or unauthorized targets.

---

## 👨‍💻 Author

**Abdul Rehman Ahmed**

BS Computer Science Student
Aspiring Cybersecurity Professional

🔐 Learning Networking, Linux, Ethical Hacking, Defensive Security, and Cybersecurity Fundamentals.
