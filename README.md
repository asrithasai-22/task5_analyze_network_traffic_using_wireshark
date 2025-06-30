# Network Traffic Analysis Report

## Overview
This report summarizes the findings from a Wireshark network traffic capture performed on host `152.57.147.112`. The analysis covers a 1-minute capture window, identifying key protocols and network activities.

## Key Findings

### Primary Protocols Identified
- **TCP**: Primary protocol for HTTP/HTTPS traffic
- **DNS**: Domain name resolution queries
- **ARP**: Address resolution for local gateway
- **HTTP**: Web browsing traffic

### Detected Network Devices
| IP Address       | Role/Identification       |
|------------------|---------------------------|
| 152.57.147.112   | Your device               |
| 152.57.147.1     | Default Gateway           |
| 8.8.8.8          | Google DNS Server         |
| 142.250.190.46   | Google Services           |

### Notable Network Activities
- **Web Browsing**:
  - HTTPS connections to Google services (port 443)
  - HTTP requests to various web servers

- **Address Resolution**:
  - ARP requests for gateway (152.57.147.1)
  - Regular ARP replies received

- **DNS Operations**:
  - Queries to Google DNS (8.8.8.8)
  - Typical response times under 50ms

## Capture Details
- **Capture Duration**: 1 minute
- **Capture Interface**: Ethernet/WiFi
- **Total Packets**: 428
- **Capture File**: `capture_152.57.147.112.pcap`

## Protocol Distribution
```mermaid
pie
    title Protocol Distribution
    "TCP" : 68
    "HTTP" : 22
    "DNS" : 7
    "ARP" : 3
