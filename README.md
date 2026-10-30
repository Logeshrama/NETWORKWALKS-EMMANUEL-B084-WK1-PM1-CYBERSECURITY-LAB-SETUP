# NETWORKWALKS-EMMANUEL-B083-WK1-PM1-CYBERSECURITY-LAB-SETUP

## Overview & Internship Context
This repository contains the documentation and completion evidence for **Week 1 - Project Module 1: Cybersecurity Lab Setup** as part of my Cybersecurity internship at **NETWORKWALKS** in collaboration with **Waqas Karim**. 

The primary objective of this project is to build practical, hands-on cybersecurity skills by designing and deploying an isolated local testing environment using **Oracle VirtualBox**. Throughout this phase, I configured a custom private network, deployed a **Kali Linux** attacking machine alongside a **Windows Pro** target virtual machine, troubleshot configuration and boot challenges, and validated bi-directional connectivity via ICMP ping tests.

---

## Lab Architecture & Network Summary
* **Hypervisor:** Oracle VirtualBox (Host: Windows)
* **Network Type:** Custom Private `NATNetwork` (Subnet: `/24`)
* **Core Components:** Kali Linux (Attacker Node) & Windows (Target Node)

---

## Phase 1: Base Environment & Kali Linux Setup
1. **VirtualBox Installation:** Installed the latest version of Oracle VirtualBox on the host system.
2. **Custom NAT Network:** Configured an isolated private virtual network (`NATNetwork`) scoped to a local subnet.
3. **Kali Linux VM:** Imported and configured the Kali Linux virtual machine as the primary penetration testing/attacking host with a static IP configuration.
4. **Integration & Workflows:** Enabled shared folders and clipboard integration to streamline host-to-guest workflows.
5. **Snapshot:** Captured a clean initial system snapshot of the Kali Linux VM.

---

## Phase 2: Windows Target VM & Connectivity Verification
1. **OS Installation:** Created a new VirtualBox VM configured with allocated RAM and a dynamically allocated VDI virtual disk using an official Windows ISO.
2. **Network Attachment:** Attached the Windows network adapter to the shared custom `NATNetwork`.
3. **Static IP Configuration:** Configured the IPv4 properties on the Windows adapter with a static address matching the local network subnet, default gateway, and DNS settings.
4. **Firewall Adjustments:** Allowed inbound ICMPv4 (Echo Request) traffic through the Windows Defender Firewall to allow bidirectional ping communication.
5. **Connectivity & Troubleshooting:** 
   * Successfully resolved initial boot and network challenges.
   * Verified internet connectivity and gateway routing from the Windows VM.
   * Executed mutual ping tests between the Windows target VM and Kali Linux, achieving **0% packet loss**.

---
## Evidence & Verification
* **LinkedIn Video Demonstration:** [Watch the lab setup and ping verification demo on LinkedIn](https://www.linkedin.com/feed/update/urn:li:activity:7521721301191802880/)
* **Status:** Successfully verified bi-directional communication between Windows 10 and Kali Linux with 0% packet loss, laying a solid foundation in Linux, virtualization, networking principles, and hands-on problem-solving.
