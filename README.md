# Securing a Small Business Network: A Hands-On Security Lab

Built, hardened, attacked, and documented a segmented small business network using KVM, OPNsense, Active Directory, and Wazuh.

## Overview

A hands-on lab where I build a small business network, harden it, attack it, and practice detecting and responding to what I find. I’m using it to learn both the offensive and defensive sides of security and to apply what I’m studying for the CompTIA Security+ exam.

**Scenario:** A 20-person company with an Active Directory domain, a public-facing web server, and no dedicated security team. My job: build the network, secure it, test it, and document everything.

## Lab Environment

| Component | Role | OS |
|---|---|---|
| Firewall | Router/firewall between zones | OPNsense |
| Domain controller | Active Directory, Group Policy | Windows Server |
| Web server | DMZ host running DVWA | Ubuntu Server |
| SIEM | Logging and detection | Wazuh |
| Attacker | Offensive testing | Kali Linux |

**Host:** Framework 16 laptop, Ubuntu, KVM/virt-manager
**Networks:** LAN (10.0.10.0/24), DMZ (10.0.20.0/24), Attacker (10.0.30.0/24), all isolated from my real network.

![Network diagram](docs/network-diagram.png)

## Project Phases

- [ ] **Phase 1: Build the network.** Segmentation, firewall rules ([write-up](docs/phase1-build.md))
- [ ] **Phase 2: Harden.** Baselines, Group Policy, before/after results ([write-up](docs/phase2-hardening.md))
- [ ] **Phase 3: Vulnerability management.** Scan, prioritize, remediate, rescan ([write-up](docs/phase3-vuln-mgmt.md))
- [ ] **Phase 4: Attack and detect.** Attacks from Kali, detection in Wazuh ([write-up](docs/phase4-attack-detect.md))
- [ ] **Phase 5: Incident response.** Full incident report ([write-up](docs/phase5-incident-response.md))
- [ ] **Phase 6: Governance and risk.** Risk register, BIA, policies ([write-up](docs/phase6-governance.md))

## Key Findings

[Fill in at the end: 3-5 bullet points, e.g. "Password spray went undetected until I tuned a Wazuh rule" or "Hardening reduced Lynis findings from X to Y."]

## Skills Demonstrated

Network segmentation, firewall configuration, system hardening (CIS), Active Directory/Group Policy, vulnerability management, SIEM monitoring, attack detection, incident response, risk assessment.

**CompTIA Security+ (SY0-701) objectives covered:** 1.3, 2.4, 2.5, 3.1, 3.2, 4.1, 4.3, 4.4, 4.6, 4.8, 4.9, 5.1, 5.2

## Tools Used

KVM/virt-manager, OPNsense, Windows Server, Ubuntu, Kali Linux, Nmap, Wireshark, OpenVAS, Lynis, Wazuh, DVWA

## What I Learned / Challenges

[Fill in at the end: what was hard, what broke, what you'd do differently.]

## Disclaimer

All attacks were performed in an isolated lab environment against systems I built and own. No real credentials, IP addresses, or personal data appear in this repository.
