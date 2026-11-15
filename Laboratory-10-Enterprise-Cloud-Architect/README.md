
# Mission 10: The Enterprise Cloud Architect

## Executive Summary
This repository contains the production-grade cloud infrastructure engineered for CloudNova Technologies' Fortune 500 client contract. The architecture delivers a highly secure, automated, resilient, and multi-tier private cloud environment deployed on a headless Ubuntu Server distribution.

The solution integrates Infrastructure as Code (IaC) via Docker Compose, host-level perimeter defense via Uncomplicated Firewall (UFW) with an enforced Default Deny policy, and zero-touch autonomous disaster recovery managed by scheduled Cron automation.

## Deliverables Index
1. **[architecture-diagram.png](architecture-diagram.png):** Visual schematic illustrating physical host, hypervisor, Linux VM, firewall layer, and container network isolation.
2. **[docker-compose.yml](docker-compose.yml):** Multi-tier orchestration file (WordPress Web Tier + MySQL Data Tier with persistent volume mounts).
3. **[automation-script.sh](automation-script.sh):** Executable Bash disaster recovery script.
4. **[operational-manual.md](operational-manual.md):** Comprehensive technical handover manual and runbook for client IT team.
5. **[final-reflection.md](final-reflection.md):** Retrospective analysis of the technical journey from Mission 1 through Mission 10.

## Infrastructure Specifications
* **Hypervisor:** Type 2 Hypervisor (Oracle VirtualBox)
* **Operating System:** Ubuntu Server (Headless)
* **Virtual Networking:** Bridged Adapter
* **Application Runtime:** Docker Engine & Docker Compose
* **Web Tier:** WordPress listening on Port 80
* **Data Tier:** MySQL 8.0 listening on Internal Port 3306 (Isolated)
* **Storage Persistence:** Named Docker Volumes (`wp_data`, `db_data`)
* **Host Security:** UFW Firewall (Default Deny; Ports 22 & 80 explicitly allowed)
* **Automation:** Cron Daemon executing daily at 02:00 AM
