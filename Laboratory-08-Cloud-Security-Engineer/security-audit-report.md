# Security Audit Report
## Mission 08 – The Cloud Security Engineer

**Student:** JHON CARLO ALLARDO  
**Course:** BS Information Technology  
**Section:** BSIT 4 B  
**Subject:** CCM101 – Cloud Computing

---

## 1. Principle of Least Privilege (PoLP)

The Principle of Least Privilege means giving users only the permissions they need to perform their assigned tasks. This is important in cloud computing because unnecessary access can expose important files, applications, and resources to unauthorized users. Limiting permissions helps reduce security risks.

## 2. Attack Surface

An attack surface refers to all possible entry points that an attacker could use to access or compromise a system. In a virtual machine, these may include open network ports, running applications, exposed services, and user accounts. Reducing unnecessary services and access points helps improve server security.

## 3. Default Deny Policy

A Default Deny policy means blocking all incoming network connections unless they are specifically allowed by the firewall. This is safer because administrators do not need to identify and block every possible attacker individually. Instead, only necessary and trusted connections are permitted.

---

## Security Audit Summary

This security audit focuses on identifying possible entry points and understanding how firewall rules help protect a cloud server. For this mission, SSH is needed for remote administration, while TCP port 8080 is required for the web application. Allowing only necessary connections helps reduce the server's attack surface and prevent unauthorized access.

## Conclusion

Through this activity, I learned that protecting a cloud server requires proper access control and firewall configuration. Applying security principles helps keep the system more secure and reduces the possibility of unauthorized connections.
