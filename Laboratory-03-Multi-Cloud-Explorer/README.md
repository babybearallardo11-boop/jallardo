# ☁️ Lab Activity 03: Multi-Cloud Explorer & Server Audit

Documentation for Mission 3 as part of the Cloud Evaluation Team at CloudNova Technologies. This repo contains our provider comparison work and basic Linux host inspection notes. 🚀

---

## 🎯 Lab Goals

- ☁️ Explore the core feature sets of AWS, Microsoft Azure, and GCP.
- 📊 Map out equivalent cloud services across providers for client recommendations.
- 🐧 Inspect system hardware and resources on a remote Linux playground.
- 📝 Build clean Markdown documentation for our GitHub portfolio.

---

## 🔍 Linux System Inspection (KillerCoda)

Ran diagnostic commands inside the KillerCoda terminal environment to gather host specs before doing provider evaluations. 

### 🖥️ System Specs Summary

| Feature | Details / Output |
| :--- | :--- |
| **OS & Kernel** 🐧 | Ubuntu 24.04.4 LTS (Noble) • `6.8.0-138-generic` |
| **Processor** ⚙️ | Intel Xeon E312xx (Sandy Bridge) @ 2.0GHz (1 vCPU, `x86_64`) |
| **RAM Space** 🧠 | 1.9 GiB total (`1.4 GiB` available, `453 MiB` used) • 1.0 GiB Swap |
| **Storage** 💾 | `/dev/vda1` root partition (~19 GB capacity) |

---

## 🛠️ Commands Executed

```bash
# Check Linux OS release info
cat /etc/os-release

# Filter CPU details
lscpu | grep -E 'Model name|CPU\(s\)|Architecture'

# Inspect current RAM usage
free -h

# Check root partition disk space
df -h /
