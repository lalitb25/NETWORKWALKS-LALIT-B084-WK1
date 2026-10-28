# 🔐 Cybersecurity Lab Environment Setup

**Building a virtual lab for cybersecurity learning and authorized security testing using Oracle VirtualBox and Kali Linux.**

## 📌 Project Overview

This project documents the setup of a virtual cybersecurity lab using Oracle VirtualBox and Kali Linux as part of NetworkWalks — Week 1, Project Module 1.

The objective is to establish a virtual environment for learning Linux networking, understanding virtual network configurations, and preparing for future cybersecurity and ethical hacking exercises.

The lab uses a custom NAT Network to provide a foundation for adding additional virtual machines for authorized security testing.

## 🎯 Project Objectives

- Install and configure Oracle VirtualBox.
- Import and configure Kali Linux as a virtual machine.
- Create a custom NAT Network using the `10.0.0.0/24` subnet.
- Configure Kali Linux with the static IPv4 address `10.0.0.2/24`.
- Configure internet connectivity for Kali Linux.
- Enable shared clipboard and drag-and-drop functionality.
- Configure a shared host folder at `/downloads` as required by the lab instructions.
- Verify IP configuration, routing, and network connectivity.
- Create a snapshot of the configured virtual machine.

## 🛡️ Purpose of the Lab

This lab provides a controlled environment for developing practical technical skills in:

- Linux system administration
- IPv4 addressing and subnetting
- Virtual network configuration
- Network connectivity troubleshooting
- Cybersecurity tool experimentation
- Future penetration-testing and security-analysis exercises

**Security note:** Only test systems you own or have explicit authorization to assess.

## 🏗️ Lab Architecture

The lab consists of a host computer running Kali Linux inside Oracle VirtualBox.

```text
             Host Computer
                   |
            Oracle VirtualBox
                   |
              NAT Network
             10.0.0.0/24
                   |
              Kali Linux
             10.0.0.2/24
```

Additional virtual machines can be connected to the same NAT Network in future exercises.

## ⚙️ Lab Configuration

| Component | Configuration |
|---|---|
| Virtualization platform | Oracle VirtualBox |
| Virtual machine | Kali Linux |
| Network mode | NAT Network |
| Network subnet | `10.0.0.0/24` |
| Kali IPv4 address | `10.0.0.2/24` |
| Subnet mask | `255.255.255.0` |
| Default gateway | Verify actual configuration |
| DNS server | Verify actual configuration |
| Shared clipboard | Bidirectional, if configured |
| Drag and drop | Bidirectional, if configured |
| Shared folder | Host `/downloads` folder |
| VM snapshot | Created after setup |

## 🪜 Implementation Steps

### Step 1: Install VirtualBox

Installed Oracle VirtualBox to provide the virtualization platform for running Kali Linux.

Official resource: https://www.virtualbox.org/wiki/Downloads

### Step 2: Create a NAT Network

Created a custom NAT Network with the required subnet:

```text
Network: 10.0.0.0/24
```

This network configuration provides a foundation for connecting multiple virtual machines to the same virtual network while supporting outbound connectivity.

### Step 3: Import Kali Linux

Imported the Kali Linux virtual machine into VirtualBox and configured its network adapter to use the custom NAT Network.

Official resource: https://www.kali.org/get-kali/

### Step 4: Configure the Kali Linux IP Address

Configured Kali Linux to use the required IPv4 address:

```text
IP Address: 10.0.0.2/24
```

The network configuration can be inspected using:

```bash
ip addr
ip route
```

These commands display the assigned IP addresses and routing information.

### Step 5: Configure Virtual Machine Integration

Configured the available VirtualBox integration features according to the lab requirements:

- Shared clipboard
- Drag and drop
- Host shared folder

These features help with transferring text and files between the host system and the virtual machine.

### Step 6: Verify Network Connectivity

Use the following commands to inspect the network configuration and test connectivity:

```bash
ip addr
ip route
ping -c 4 8.8.8.8
ping -c 4 google.com
```

The ping tests help distinguish basic IP connectivity issues from DNS resolution issues.

Record the actual results in the project documentation after running the commands.

### Step 7: Create a Virtual Machine Snapshot

Created a snapshot of the configured Kali Linux virtual machine to provide a recovery point before future lab exercises.

Suggested snapshot name:

```text
WK1-PM1-Complete
```

## 🔎 Verification Checklist

| Check | Command or location | Status |
|---|---|---|
| Kali IP address | `ip addr` | Verify |
| Network route | `ip route` | Verify |
| Internet connectivity | `ping -c 4 8.8.8.8` | Verify |
| DNS resolution | `ping -c 4 google.com` | Verify |
| NAT Network subnet | VirtualBox network settings | Verify |
| Clipboard and drag-and-drop | VM settings | Verify |
| Shared folder | VM settings and Kali | Verify |
| Snapshot | VirtualBox Snapshots | Verify |

## 🐞 Troubleshooting

Network configuration issues can arise when the virtual network and the Kali Linux network settings do not match.

A systematic troubleshooting approach is:

1. Inspect the assigned IP address using `ip addr`.
2. Check the default route using `ip route`.
3. Verify the NAT Network subnet in VirtualBox.
4. Test connectivity to an IP address.
5. Test DNS resolution using a domain name.
6. Recheck the network configuration and restart the connection if necessary.

Document any problems encountered, their actual causes, the steps taken to resolve them, and the results.

## 💡 Key Learning Outcomes

Through this project, I practised the fundamentals of setting up a virtual cybersecurity environment.

Key areas of learning include:

1. **Virtualization:** Running a Linux operating system inside a virtual machine.
2. **Virtual networking:** Configuring a NAT Network for lab connectivity.
3. **IPv4 configuration:** Understanding IP addresses and subnet masks.
4. **Network troubleshooting:** Inspecting interfaces, routes, and connectivity.
5. **Virtual machine management:** Configuring integration settings and snapshots.
6. **Technical documentation:** Recording configuration details and verification results.

## 🔐 Security and Ethical Use

This environment is intended for educational purposes and authorized security testing.

Any future scanning, vulnerability assessment, or penetration-testing exercises should be restricted to systems you own, intentionally vulnerable lab machines, or systems for which you have explicit authorization.


## 🔗 Tools and Resources

- [Oracle VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Kali Linux](https://www.kali.org/get-kali/)
- [NetworkWalks](https://www.networkwalks.com/)

## 👤 Author

**Lalit Bharambe**

Cybersecurity Learner

Project: NetworkWalks — Week 1, Project Module 1

Platform: Oracle VirtualBox and Kali Linux

## 📌 Project Information

| Field | Details |
|---|---|
| Program | NetworkWalks Cybersecurity |
| Week | 01 |
| Project Module | 01 |
| Project | VirtualBox and Kali Linux Lab Setup |
| Network | `10.0.0.0/24` |
| Kali IP | `10.0.0.2/24` |

---

