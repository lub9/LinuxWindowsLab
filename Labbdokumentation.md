
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

## Ubuntu Server

The Ubuntu Server was configured with a static IP address.

Hostname: admin-virtualbox
IP Address: 192.168.10.10
Subnet Mask: 255.255.255.0
Default Gateway: None

The network configuration was checked using:

ip addr

The output showed that the Ubuntu server had the IP address 192.168.10.10/24.

The /24 notation corresponds to the subnet mask 255.255.255.0.

![Ubuntu IP configuration](Picture/Screenshot 2026-09-17 110925.png)

## Windows Client

The Windows client was configured with a static IP address.

Hostname: Windows-Client
IP Address: 192.168.10.20
Subnet Mask: 255.255.255.0
Default Gateway: None

The IP configuration was checked using:

ipconfig

## Communication Between the Virtual Machines

The connection between the two virtual machines was tested using ping.

Ubuntu → Windows

The following command was executed on Ubuntu:

ping -c 4 192.168.10.20

The Ubuntu server received replies from the Windows client.

Example:

64 bytes from 192.168.10.20
64 bytes from 192.168.10.20
64 bytes from 192.168.10.20
64 bytes from 192.168.10.20

This confirms that the Ubuntu server can communicate with the Windows client over the internal network.

## Windows → Ubuntu

The following command was executed on Windows:

ping 192.168.10.10

The Windows client received replies from the Ubuntu server.

Example:

Reply from 192.168.10.10: bytes=32 time<1ms TTL=64
Reply from 192.168.10.10: bytes=32 time<1ms TTL=64
Reply from 192.168.10.10: bytes=32 time<1ms TTL=64
Reply from 192.168.10.10: bytes=32 time<1ms TTL=64

This confirms that communication works in both directions.

## Windows → Ubuntu

The following command was executed on Windows:

ping 192.168.10.10

The Windows client received replies from the Ubuntu server.

Example:

Reply from 192.168.10.10: bytes=32 time<1ms TTL=64
Reply from 192.168.10.10: bytes=32 time<1ms TTL=64
Reply from 192.168.10.10: bytes=32 time<1ms TTL=64
Reply from 192.168.10.10: bytes=32 time<1ms TTL=64

This confirms that communication works in both directions.

## Result

The two virtual machines were successfully configured on the same internal network.

Communication between the Ubuntu Server and Windows Client was verified using ping in both directions.

Results:

Ubuntu Server can communicate with the Windows Client.
Windows Client can communicate with the Ubuntu Server.
Both machines use the same subnet.
The Windows Firewall was configured to allow ICMPv4 Echo Requests.
The LabNetwork internal network is functioning correctly.

## 3. Command-Line Implementation and Troubleshooting

### 3.1 Linux - Bash

### 3.2 Windows - PowerShell

## 4. Git and Version Control

## 5. AI Log and Critical Evaluation