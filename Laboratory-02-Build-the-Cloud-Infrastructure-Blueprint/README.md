
# CCM101 Cloud Computing Laboratory

## Mission Overview

This laboratory mission focused on exploring a cloud-based Linux server and understanding the basic parts of cloud infrastructure. Using the KillerCoda terminal, I investigated the server environment and collected information about its operating system, hardware, storage, file systems, hostname, and network configuration. The activity also helped me practice documenting technical information and organizing my work in GitHub.

## Objectives

* Explore and inspect a Linux cloud server.
* Identify the basic cloud infrastructure components.
* Practice using Linux commands through the terminal.
* Check the server's hardware, storage, and network information.
* Document the results of the investigation.
* Improve my technical documentation and GitHub portfolio.

## Cloud Infrastructure Components

The main cloud infrastructure components explored during the mission were:

* **Compute** – The server's CPU and available processing resources.
* **Storage** – The disk space and partitions used by the Linux system.
* **Network** – The network interface and IP address used by the server.
* **Operating System** – Ubuntu 24.04.4 LTS running the cloud server.
* **File Systems** – The mounted partitions and system file systems used by Linux.

## Tools Used

* **KillerCoda** – Used to access and investigate the cloud-based Linux environment.
* **Linux Terminal** – Used to execute commands and collect system information.
* **GitHub** – Used to store and organize the laboratory documentation and results.
* **Markdown** – Used to format the laboratory README and reports.

## Linux Commands Executed

The following commands were used during the investigation:

```bash
lsb_release -ds
uname -r
lscpu
free -h
df -h
findmnt
hostname
hostname -I
ip addr
nproc
```

These commands were used to identify the operating system, kernel, processor, memory, disk usage, mounted file systems, hostname, CPU cores, and network configuration.

## Skills Learned

During this laboratory, I learned how to navigate and investigate a Linux server through the command line. I practiced reading system information and identifying important infrastructure details such as RAM, CPU, storage, and IP addresses. I also improved my Markdown formatting and learned how to present technical findings in a more organized way. Another skill I developed was documenting command outputs so they can be reviewed later.

## Challenges Encountered

One challenge was understanding the information displayed by some Linux commands because the output contained technical terms and several different system components. I also had to determine which IP address represented the main network connection because the server had both a primary network interface and a Docker interface. Another challenge was making sure that the collected information was recorded accurately in the laboratory documentation. By checking the command outputs carefully, I was able to organize the results and complete the investigation.
