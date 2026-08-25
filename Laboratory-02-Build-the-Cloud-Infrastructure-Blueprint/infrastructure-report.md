
# Checkpoint 2 – Cloud Server Investigation

## Overview

The KillerCoda terminal was used to investigate the Linux cloud server environment. The investigation identified the operating system, kernel version, CPU, memory, disk storage, mounted file systems, hostname, and IP address.

## System Information

| Component         | Finding                                       |
| ----------------- | --------------------------------------------- |
| Operating System  | Ubuntu 24.04.4 LTS                            |
| Kernel Version    | 6.8.0-138-generic                             |
| CPU Model         | Intel Xeon E312xx (Sandy Bridge, IBRS update) |
| CPU Cores         | To be obtained using `nproc`                  |
| Total RAM         | 1.9 GiB                                       |
| Disk Capacity     | 19 GB main filesystem (`/dev/vda1`)           |
| Hostname          | ubuntu                                        |
| IP Address        | 172.30.1.2                                    |
| Network Interface | enp1s0                                        |

## Disk and Mounted File Systems

The main filesystem is `/dev/vda1`, which has a capacity of 19 GB. It is mounted at `/` and uses the ext4 filesystem.

Other mounted partitions include:

* `/dev/vda16` – 881 MB, mounted at `/boot`
* `/dev/vda15` – 105 MB, mounted at `/boot/efi`
* `tmpfs` – mounted at `/run`
* `tmpfs` – mounted at `/dev/shm`
* `tmpfs` – mounted at `/run/lock`
* System filesystems including `/proc`, `/sys`, and `/dev`

## Network Information

The server hostname is `ubuntu`.

The primary network interface is `enp1s0`, with the IP address:

`172.30.1.2/24`

A Docker network interface is also present with the address:

`172.17.0.1/16`

The loopback interface uses `127.0.0.1`.

## Commands Used

The following Linux commands were used during the investigation:

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
```

To determine the number of CPU cores, the following command should also be executed:

```bash
nproc
```

## Summary

The KillerCoda cloud server is running Ubuntu 24.04.4 LTS with kernel version 6.8.0-138-generic. It has an Intel Xeon E312xx processor, approximately 1.9 GiB of RAM, and a 19 GB main filesystem. The hostname is `ubuntu`, and its primary IP address is `172.30.1.2`.

Screenshots of the terminal investigation should be included as evidence for the recorded findings.
