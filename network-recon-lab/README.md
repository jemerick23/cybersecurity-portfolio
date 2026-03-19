# Network Reconnaissance Lab

This lab demonstrates network reconnaissance techniques using Kali Linux and Nmap. The objective was to identify active hosts, validate target systems, enumerate services, and analyze security exposure on a local network.

## Objective

Identify devices on the network and discover open ports.

## Tools Used

- Kali Linux
- Nmap

## Methodolgy

### 1. Network Discovery 

A ping sweep was conducted to identify active hosts on the local network.

### 2. Target Validation

Discovered hosts were analyzed to determine the correct lab target. This step highlights the importance of verifying assets before conducting deeper analysis.

### 3. Host Enumeration (Discovered System)

An identified host (192.168.1.100) was scanned to enumerate open ports, services, and operating system details.

### 4. Controlled Target Analysis

A confirmed lab system (HOME-SOC-1) was scanned to compare security posture.

## Key Findings

### Discovered Host (192.168.1.100)

- Multiple open ports identified:
  - 135 (MSRPC)
  - 139 (NetBIOS)
  - 445 (SMB)
  - 445 (SMB)
  - 5985 (WinRM)
- Indicators of a Windows-based system
- Internal domain information observed through network services
- SMB configuration suggests potential for relay-based attacks

### Lab Host (HOME-SOC-1)

- All scanned ports were filtered
- No externally exposed services detected
- OS fingerprinting was limited due to restricted responses

### Security Analysis

The comparison between the two systems highlights the impact of configuration and exposure:

- The discovered host presents a larger attack surface due to multiple exposed services
- The lab system demonstrates a hardened posture with minimal network visibility
- Network reconnaissance can reveal critical system details even without exploitation

### Conslusion

This lab demonstrates the importance of:

- Accurate target identification
- Service and port enumeration
- Understanding network exposure
- Comparing system security posture

These techniques are foundational for both defensive security monitoring and offensive security assessments.

## Status

Lab setup in progress.
