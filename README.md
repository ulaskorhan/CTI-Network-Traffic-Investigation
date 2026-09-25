# CTI Network Traffic Investigation

## Overview

This project is a practical Cyber Threat Intelligence (CTI) investigation of network traffic using publicly available network traffic data.

The objective is to investigate network activity, identify potentially suspicious behavior, extract relevant indicators, map observed behavior to MITRE ATT&CK techniques where supported by evidence, and produce a structured technical intelligence report.

The project is designed as a practical demonstration of network traffic analysis, threat intelligence analysis, evidence-based assessment, and technical reporting.

## Objectives

The investigation will focus on:

- Analyzing network traffic from a public PCAP dataset
- Identifying hosts, protocols, connections, and communication patterns
- Investigating DNS, HTTP, TLS, and other relevant network activity
- Identifying potentially suspicious network behavior
- Extracting and documenting Indicators of Compromise (IOCs)
- Mapping observed behavior to MITRE ATT&CK techniques where appropriate
- Developing a timeline of relevant network activity
- Assessing findings and confidence levels
- Identifying intelligence gaps and analytical limitations
- Producing a structured technical CTI report

## Methodology

The investigation will follow an evidence-based workflow:

1. Dataset identification and documentation
2. Initial network traffic overview
3. Packet-level analysis
4. Structured network analysis
5. IOC identification and enrichment
6. Behavioral analysis
7. MITRE ATT&CK mapping
8. Timeline development
9. Intelligence assessment
10. Technical reporting

Findings will be distinguished from observations and assessments, and conclusions will be based on available evidence.

## Tools

The project uses:

- Wireshark
- TShark
- Zeek
- Python
- MITRE ATT&CK

Additional tools or data sources may be introduced during the investigation where relevant.

# CTI-Network-Traffic-Investigation
A practical Cyber Threat Intelligence investigation of network traffic using PCAP, Wireshark, Zeek and Python.

## Repository Structure

```text
CTI-Network-Traffic-Investigation/
│
├── data/
│   └── README.md
│
├── analysis/
│   ├── wireshark/
│   ├── zeek/
│   └── python/
│
├── iocs/
│   └── iocs.csv
│
├── reports/
│   └── technical-report.md
│
├── screenshots/
│
├── references/
│   └── sources.md
│
└── README.md



