# Defensive Security Plan - Network Scanning Lab

## 1. Overview
This document outlines the strategic defensive measures required to secure the host `scanme.nmap.org` based on the findings from the vulnerability analysis. The goal is to minimize the attack surface and strengthen the overall security posture.

## 2. Technical Mitigation Strategy

### Phase 1: Patch Management
* **Immediate Action:** Execute a full system update to patch the identified vulnerabilities in **OpenSSH 6.6.1p1** and **Apache 2.4.7**.
* **Command:** `sudo apt update && sudo apt upgrade -y`
* **Goal:** Transition to the latest stable versions to remediate known CVEs (e.g., CVE-2016-10009).

### Phase 2: Service Hardening (Reduce Information Leakage)
To prevent "Banner Grabbing" and reconnaissance by attackers:

| Service | Action | Configuration Change |
| :--- | :--- | :--- |
| **Apache** | Hide Version Info | Set `ServerTokens Prod` and `ServerSignature Off` |
| **SSH** | Secure Access | Disable `RootLogin`, change default port (optional), and use SSH Keys. |
| **Nping** | Disable Diagnostic | Stop and disable the `nping-echo` service if not required. |

### Phase 3: Network Security & Firewall (UFW/Iptables)
Implement a **Whitelisting** approach instead of Blacklisting:
1.  **Restrict SSH:** Only allow SSH access from specific trusted IP addresses.
2.  **Close Unnecessary Ports:** Use a firewall to block ports `9929` and `31337`.
3.  **Command Example:**
    ```bash
    sudo ufw default deny incoming
    sudo ufw allow from [Your_IP] to any port 22
    sudo ufw allow 80/tcp
    sudo ufw enable
    ```

## 3. Monitoring & Detection
* **Intrusion Detection (IDS):** Deploy **Fail2Ban** to automatically block IPs that exhibit malicious behavior (e.g., repeated failed SSH login attempts).
* **Log Analysis:** Regularly monitor `/var/log/auth.log` and `/var/log/apache2/access.log` for suspicious patterns.

## 4. Conclusion
By implementing these defensive layers, the risk of exploitation is significantly reduced. Security is a continuous process, and regular scanning with tools like Nmap should be part of the monthly maintenance routine.

---
**Plan Prepared By:** Shrouq Al-Mejireshi
