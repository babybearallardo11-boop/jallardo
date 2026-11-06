# FIREWALL CONFIGURATION DOCUMENTATION

## Mission 08 – The Cloud Security Engineer

**Student:** JHON CARLO ALLARDO  
**Course:** BS Information Technology  
**Year & Section:** BSIT 4 B  
**Institution:** University of Eastern Pangasinan  
**Subject:** CCM101 – Cloud Computing

## Introduction

Firewall configuration is an important part of protecting a cloud server from unauthorized access and unwanted network traffic. In this laboratory, I used UFW (Uncomplicated Firewall) in an Ubuntu environment to manage network connections and secure a deployed Nginx web application.

The main goal was to apply a Default Deny policy, allow SSH for remote administration, and permit TCP port 8080 for the web application.

## 1. Allow SSH Access

**Command:** `sudo ufw allow ssh`

This command allows incoming SSH connections through port 22. SSH is important because it allows administrators to remotely access and manage the server. This rule must be added before enabling the firewall to avoid accidentally losing remote access.

## 2. Configure Default Deny Policy

**Block incoming connections:**

`sudo ufw default deny incoming`

This command blocks incoming network connections unless they are specifically allowed.

**Allow outgoing connections:**

`sudo ufw default allow outgoing`

This command allows the server to communicate with external services, download updates, and access necessary online resources.

These settings follow the Default Deny approach, where only required incoming connections are permitted.

## 3. Enable the Firewall

**Command:** `sudo ufw enable`

This command activates the UFW firewall. If a confirmation message appears, I must enter Y to continue.

**Verification command:** `sudo ufw status verbose`

This command displays the current firewall status, default policies, and active rules. The expected status is active, with incoming traffic denied and outgoing traffic allowed.

## 4. Allow Application Traffic on Port 8080

**Command:** `sudo ufw allow 8080/tcp`

This command allows incoming TCP connections through port 8080, which is mapped to the Nginx web server running inside the Docker container.

Allowing this specific port makes the application accessible through its designated service port without unnecessarily opening other ports.

## 5. Verify Firewall Rules

**Command:** `sudo ufw status numbered`

This command displays all configured firewall rules with their corresponding numbers. The expected rules include port 22 for SSH and port 8080 for the web application.

The numbered list makes it easier to review and manage the firewall configuration.

## 6. Test the Web Application

**Command:** `curl http://localhost:8080`

This command sends a request to the locally deployed Nginx application. A successful response should display the HTML content of the Nginx welcome page.

This confirms that the application is responding to local requests. However, a successful localhost request alone does not prove that external traffic can reach the application.

## 7. Security Considerations

Enabling UFW before allowing SSH may block incoming SSH connections because of the Default Deny policy. This could prevent administrators from remotely accessing the server.

Some important security practices include:

1. Allow only the ports required by the application.
2. Avoid exposing unnecessary services.
3. Use strong authentication.
4. Regularly review firewall rules.
5. Keep the operating system and applications updated.
6. Monitor unusual network activity.
7. Follow the Principle of Least Privilege.

## 8. Commands Summary

| Command | Purpose |
|---|---|
| `sudo ufw allow ssh` | Allows SSH access |
| `sudo ufw default deny incoming` | Blocks incoming traffic by default |
| `sudo ufw default allow outgoing` | Allows outgoing traffic |
| `sudo ufw enable` | Activates UFW |
| `sudo ufw status verbose` | Checks firewall status |
| `sudo ufw allow 8080/tcp` | Allows TCP port 8080 |
| `sudo ufw status numbered` | Displays numbered firewall rules |
| `curl http://localhost:8080` | Tests the Nginx application |

## Conclusion

Through this laboratory activity, I learned how to configure a firewall and manage network access on an Ubuntu server. I understood why SSH must be allowed before activating UFW and how a Default Deny policy helps prevent unnecessary incoming connections. I also gained experience in allowing specific application ports and checking firewall rules using Linux commands. This activity showed me that protecting a cloud server requires proper configuration, monitoring, and responsible management of network access.
