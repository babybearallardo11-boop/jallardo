# ☁️ LABORATORY 08: THE CLOUD SECURITY ENGINEER

### CCM101 – Cloud Computing
**College of Information Technology**

---

## 👨‍🎓 Student Information

| Details | Information |
|---|---|
| Name | JHON CARLO ALLARDO |
| Course | BS Information Technology |
| Year & Section | BSIT 4 B |
| Institution | University of Eastern Pangasinan |
| Academic Year | 2026–2027 |
| Laboratory | 08 – Cloud Security Engineer |

---

## 🎯 Mission Overview

This laboratory focuses on securing a Linux server using
the Uncomplicated Firewall (UFW). The mission involves
deploying a web application, checking active network
ports, and configuring firewall rules to control incoming
and outgoing traffic.

Through this activity, I learned how important it is to
protect cloud servers from unauthorized access while
allowing legitimate users to access necessary services.

## 🚀 Mission Objectives

- Understand the Principle of Least Privilege.
- Identify the attack surface of a virtual machine.
- Perform a basic network security audit.
- Configure UFW with a Default Deny policy.
- Allow SSH and HTTP application traffic.
- Document firewall configurations and security practices.

## 🛠️ Tools Used

- KillerCoda Playground
- Ubuntu Linux
- Docker
- Nginx
- UFW Firewall
- Git and GitHub
- cURL

## 💻 Commands Executed

```bash
docker run -d --name secure-web-app -p 8080:80 nginx
curl http://localhost:8080
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose
sudo ufw allow 8080/tcp
sudo ufw status numbered
curl http://localhost:8080
