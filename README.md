# Network Traffic Analysis Using Wireshark

## Project Overview

This project demonstrates practical network traffic analysis using Wireshark on Windows 11. It covers packet capture, protocol identification, TCP connection establishment, DHCP traffic inspection, TCP and UDP packet analysis, TCP retransmission filtering, and protocol statistics.

## Objectives

- Capture and inspect network packets using Wireshark.
- Identify ICMP Echo Request and Echo Reply packets.
- Examine DNS Query and DNS Response traffic.
- Analyze the TCP three-way handshake.
- Inspect DHCP Request and ACK packets.
- Examine TCP flags, port numbers, and UDP packet length.
- Identify TCP retransmission-related packets.
- Compare TCP and UDP traffic statistics.

## Tools and Environment

- **Operating System:** Windows 11
- **Packet Analyzer:** Wireshark
- **Capture Support:** Npcap
- **Network Interface:** Wi-Fi

## Practical Activities and Results

### Practical 01: ICMP and DNS Analysis

- ICMP Echo Request and Echo Reply packets were observed.
- DNS Query and DNS Response packets were observed.
- The packet capture was saved.

### Practical 02: TCP Three-Way Handshake

- The SYN, SYN-ACK, and ACK stages were identified.
- The inspected TCP stream was stream 10.
- The handshake packets were recorded as packets 35, 37, and 39, respectively.

### Practical 03: DHCP Analysis

- DHCP Request and DHCP ACK packets were observed.
- The DHCP message types and transaction information were inspected.
- The complete Discover–Offer–Request–ACK sequence was not confirmed.

### Practical 04: TCP and UDP Analysis

**Observed TCP packet**

| Field | Value |
|---|---|
| Source port | 443 |
| Destination port | 50698 |
| TCP flags | PSH, ACK |

**Observed UDP packet**

| Field | Value |
|---|---|
| Source port | 51957 |
| Destination port | 53 |
| UDP length | 46 bytes |
| Protocol column | UDP |

These values describe the selected packets only. The UDP packet's DNS-layer decoding was not recorded as confirmed.

### Practical 05: TCP Retransmission Analysis

- Display filter: `tcp.analysis.retransmission`
- Matching packets: 67
- TCP stream index: 1
- Observed source port: 443
- The field associated with port value 50644 was not confirmed.
- The cause and impact of the retransmissions were not established.

### Practical 06: Protocol Hierarchy Analysis

| Measurement | TCP | UDP |
|---|---:|---:|
| Packets | 2,461 | 248 |
| Bytes | 51,628 | 1,984 |

TCP had a higher packet count and recorded byte total than UDP in the selected capture. Conversations details were not recorded.

## Repository Structure

```text
Network-Traffic-Analysis/
├── captures/
├── screenshots/
├── report/
└── documentation/
    └── README.md
```

## Limitations

- Results are limited to the selected captures and observed packets.
- The complete DHCP DORA sequence was not confirmed.
- The selected UDP packet was not documented as a confirmed DNS message.
- The cause of the TCP retransmission-filter matches was not established.
- Conversations statistics were not recorded.
- Traffic statistics may differ between captures or when display filters are applied.

## Security and Privacy

Packet captures can contain IP addresses, MAC addresses, DNS queries, hostnames, and other sensitive information. Review captures and screenshots before publishing. Do not upload raw capture files to a public repository unless they have been checked for sensitive data and are appropriate to share.

## Conclusion

This project provided hands-on experience using Wireshark to inspect common network protocols, examine TCP and UDP packet fields, identify TCP handshake and retransmission-related traffic, and summarize protocol statistics.

The documented findings are limited to the observations recorded during the practical activities.

## Author

**Name:** [Your Name]

**Project:** Network Traffic Analysis Using Wireshark

