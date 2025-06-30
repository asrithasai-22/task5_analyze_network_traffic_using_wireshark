# Network Traffic Analysis Report

## Overview
This report summarizes the findings from a Wireshark network traffic capture performed on the `192.168.29.0/24` subnet. The analysis covers a 1-minute capture window, identifying key protocols, devices, and network activities.

## Key Findings

### Primary Protocols Identified
- **UDP**: Dominant protocol for DNS queries and other services
- **ARP**: Address resolution between local devices
- **IGMPv3**: Multicast group management
- **ICMPv6**: IPv6 neighbor discovery and router communications

### Detected Network Devices
 IP Address        Role/Identification       
---------------------------------------------
 192.168.29.1      Default Gateway           
 192.168.29.152    Local device (unidentified)
 192.168.29.171    Local device (unidentified)
 224.0.0.251       mDNS multicast address    
 ff02::1           IPv6 All-Nodes multicast  

### Notable Network Activities
- **DNS Operations**:
  - Queries to Google DNS (8.8.8.8)
  - Local mDNS (.local) name resolution

- **Address Resolution**:
  - ARP requests/replies for MAC address mapping
  - ICMPv6 neighbor discovery

- **Multicast Activities**:
  - IGMPv3 membership reports
  - IPv6 router advertisements

## Capture Details
- **Capture Duration**: 1 minute
- **Capture Interface**: Ethernet/WiFi (auto-detected)
- **Total Packets**: 347
- **Capture File**: `network_capture_20240630.pcap`

## Protocol Distribution
```mermaid
pie
    title Protocol Distribution
    "UDP" : 42
    "ARP" : 28
    "IGMPv3" : 15
    "ICMPv6" : 10
    "Other" : 5
