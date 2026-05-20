# Network Scanning & Vulnerability Analysis Lab 🔍

![Nmap](https://img.shields.io/badge/Tools-Nmap-blue) ![Security](https://img.shields.io/badge/Focus-Network--Security-green) ![Status](https://img.shields.io/badge/Status-Completed-success)

## Project Description
A comprehensive security assessment of `scanme.nmap.org` using industry-standard tools to identify open services, operating system details, and potential security risks. This lab demonstrates the fundamental stages of reconnaissance and network enumeration.

## Technical Evidence Gallery

| 1. Port Identification | 2. Service Discovery |
|---|---|
| ![Ports](screenshots/ports.png) | ![Services](screenshots/services.png) |

| 3. OS Fingerprinting | 4. Version Analysis |
|---|---|
| ![OS](screenshots/os.png) | ![Versions](screenshots/versions.png) |

## Executive Analysis

During this assessment, I utilized advanced Nmap flags to extract deep technical data while maintaining scan efficiency.

### Key Findings:
- **Service Enumeration:** Successfully identified open ports such as **SSH (22)** and **HTTP (80)**, including their specific version numbers.
- **OS Fingerprinting:** Discovered the target is running a **Linux-based** kernel, allowing for targeted vulnerability research.
- **Aggressive Scanning:** Used the `-A` flag to automate traceroute, OS detection, and common script scanning (NSE).

## Project Structure

- **[Main Scan Results](my_scan_results.txt)** - The primary output of the comprehensive scan.
- **[Analysis Report](report/analysis_report.md)** - Detailed breakdown of findings and risk assessment.
- **[Defensive Plan](report/defensive_plan.md)** - Recommended security controls to mitigate discovered risks.
- **[Evidence](screenshots/)** - Visual confirmation of the terminal outputs.

## Methodology
1. **Reconnaissance:** Host discovery and reachability testing.
2. **Stealth Scanning:** Utilizing SYN scans (`-sS`) to analyze ports.
3. **Deep Analysis:** Version detection (`-sV`) and OS identification (`-O`) for precise mapping.

---
*Developed by Shrouq Almejireshi as part of Cybersecurity Professional Training.*
