
# Checkpoint 3 – Cloud Infrastructure Components

## 1. Compute Resource

**Linux Example:** Processor / CPU

**What it does:**
The CPU is responsible for processing instructions and performing the operations required by the Linux system. It allows applications, commands, and background processes to run.

**Why it matters in Cloud Computing:**
Compute power is one of the most important resources in cloud computing because applications need processing capacity to handle different workloads. Cloud providers can adjust computing resources depending on the needs of an application.

**KillerCoda Example:**
The processor information of the KillerCoda environment can be viewed by running:

```bash
lscpu
```

This displays information such as the CPU architecture, number of CPUs, and processor details.

---

## 2. Storage Resource

**Linux Example:** Disk / File System

**What it does:**
Storage is where the operating system, programs, configuration files, and user data are kept. It provides space for information that needs to be saved and accessed later.

**Why it matters in Cloud Computing:**
Cloud applications generate and store large amounts of information. Storage resources allow files, databases, application data, and other important information to remain available when needed.

**KillerCoda Example:**
The available disk space can be checked using:

```bash
df -h
```

This command shows the file systems, their total capacity, used space, available space, and usage percentage.

---

## 3. Network Resource

**Linux Example:** Network Interface / IP Address

**What it does:**
The network resource allows the Linux system to communicate with other computers, servers, and online services. An IP address identifies the system within a network.

**Why it matters in Cloud Computing:**
Cloud systems depend heavily on networking because users and applications need to communicate with cloud servers and services. Without a network connection, cloud resources would not be accessible or able to exchange information.

**KillerCoda Example:**
The IP address and network interfaces can be viewed using:

```bash
hostname -I
ip addr
```

`hostname -I` displays the assigned IP address, while `ip addr` provides more detailed information about the available network interfaces.

---

## 4. Operating System

**Linux Example:** Linux Operating System

**What it does:**
The operating system serves as the main software layer between the hardware and the applications. It manages system resources and provides users with tools for interacting with the computer.

**Why it matters in Cloud Computing:**
Cloud servers need an operating system to manage their resources and run different services. Linux is widely used in cloud environments because it is lightweight, reliable, customizable, and suitable for server workloads.

**KillerCoda Example:**
KillerCoda provides a Linux-based environment where users can interact with the system using terminal commands. Through this environment, users can examine resources such as the CPU, disk, network, and other system information.

---

## Summary

The different infrastructure components work together to create a functioning cloud environment. The **CPU** provides processing power, **storage** keeps files and data, **networking** allows communication, and the **Linux operating system** manages these resources. By using KillerCoda, these components can be explored through actual Linux commands, giving a practical understanding of how cloud infrastructure operates.
