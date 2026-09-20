
# Linux and Windows Virtual Lab

## 1. Introduction.

Name: Lubna Rabia   
Date: September 14, 2026
Course:Introduktion till yrkesrollen och grunderna i IT-infrastruktur (ISCX26, Chas Academy)

Description:
This project documents a virtual lab containing an Ubuntu
Linux server and a Windows client connected through a
shared virtual network.

| Hostname       | Operating System | IP Address   | Subnet Mask   | Default Gateway |
| -------------- | ---------------- | ------------ | ------------- | --------------- |
| admin-virtualbox   | ubuntu 26.04 LTS    | 192.168.10.10 | 255.255.255.0 | —               |
| windows-client | Windows 11       | 192.168.10.20 | 255.255.255.0 | —               |

## 2. Lab Environment and Network


Two virtual machines were created using VirtualBox:

A Linux server running Ubuntu Server.
A Windows client running Windows 11.

Both virtual machines were connected to the same internal network in VirtualBox.

Network Configuration

Network name: LabNetwork
Network type: Internal Network

Both virtual machines use the same internal network and can therefore communicate with each other.

Ubuntu Server

The Ubuntu Server was configured with a static IP address.

Hostname: admin-virtualbox
IP Address: 192.168.10.10
Subnet Mask: 255.255.255.0
Default Gateway: None

The network configuration was checked using:

ip addr

The output showed that the Ubuntu server had the IP address 192.168.10.10/24.

The /24 notation corresponds to the subnet mask 255.255.255.0.



## 3. Command-Line Implementation and Troubleshooting

### 3.1 Linux - Bash

### 3.2 Windows - PowerShell

## 4. Git and Version Control

## 5. AI Log and Critical Evaluation