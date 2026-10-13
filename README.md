# OPNsense Network Security Architecture (Zero Trust) 🛡️

**DUT Génie Informatique - Final Year Project (PFE) @ EST Salé**

👨‍💻 **Authors:** Othman Benyahya & Lhachimi Mohamed Yassine[cite: 1]  
🎓 **Supervisors:** Pr. Ali Lasfar & Pr. Younes Lourtassi[cite: 1]

📥 **[Click here to view the Full Project Report (PDF)](./Rapport_PFE_OPNsense.pdf)** 

## 📌 Overview
This repository contains the comprehensive documentation for our final year infrastructure project[cite: 1]. The project focuses on designing, deploying, and testing an enterprise-grade, multi-site network security architecture using **OPNsense** and **VirtualBox**[cite: 3, 31]. 

To counter modern cyber threats, we moved away from traditional perimeter security and implemented an architecture based on **Defense in Depth** and **Zero Trust** paradigms[cite: 3]. Every network flow is inspected, legitimized, and strictly segmented[cite: 12].

## 🚀 Key Objectives & Achievements
We built this infrastructure from scratch in a virtualized lab environment, successfully implementing the following enterprise features:

*   **Zero Trust Micro-segmentation:** Strict isolation of our environments into LAN (Users), DMZ (Exposed Services), SRV (Databases), and MGMT (Administration) using a "Deny by Default" policy[cite: 3, 24, 25].
*   **High Availability (Multi-WAN):** Configured traffic shaping, Load Balancing (Active/Active), and Failover (Active/Passive) mechanisms to ensure continuous internet availability[cite: 3, 41, 42].
*   **Site-to-Site VPN:** Established a secure OpenVPN cryptographic tunnel backed by a custom Public Key Infrastructure (PKI) to safely connect our Main Site and Remote Server Site[cite: 3, 43].
*   **Application-Level Web Filtering:** Deployed a Squid Proxy (Transparent on the main site, Explicit on the remote site) with SSL Bumping to inspect encrypted HTTPS traffic and block malicious categories[cite: 3, 52, 54].
*   **Intrusion Prevention System (IPS):** Integrated Suricata with Emerging Threats (ET Telemetry) signatures and custom rules to actively detect and drop malicious behaviors, such as aggressive Nmap scans[cite: 3, 56, 57].

## 🛠️ Technologies & Tools Stack
*   **Firewall & Routing:** OPNsense[cite: 31]
*   **Virtualization:** Oracle VM VirtualBox[cite: 31]
*   **Security Modules:** Suricata (IDS/IPS), OpenVPN, Squid Proxy[cite: 33, 34]
*   **Servers & OS:** Ubuntu Server, Kali Linux, Lubuntu, Apache Tomcat, MariaDB[cite: 32]
*   **Auditing:** Nmap, FileZilla[cite: 34]

## 📖 What's Inside the Report
Since this project was fully virtualized and configuration-based, our complete engineering process is documented in the attached PDF[cite: 1, 30]. Inside, you will find:
1.  **Network Architecture Diagrams:** Detailed visual topologies of the simulated enterprise network[cite: 25].
2.  **Security Policies:** Comprehensive matrices of our inter-zone firewall rules[cite: 27].
3.  **Step-by-Step Implementation:** Configurations for gateway groups, VPN certificates, NAT port forwarding, and Suricata IPS[cite: 42, 43, 53, 56].
4.  **Validation & Red Teaming:** Real-world tests proving the resilience of the network, including simulated hardware failures and Nmap intrusion attempts from our Kali Linux machine[cite: 3, 62, 68].

---
*Note: The complete lab environments, configurations, and test screenshots are compiled within the `Rapport_PFE_OPNsense.pdf` file linked at the top of this page.*
