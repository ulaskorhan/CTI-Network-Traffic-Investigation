# Technical Network Traffic Investigation

## 1. Investigation Scope

This investigation examines the network traffic contained in the selected CTU-IDSEVAL-6 malware capture:

`ctu-idseval-6-malicious-malware-1.pcap`

The purpose is to identify and characterize potentially suspicious network behavior using packet-level and structured network analysis.

The investigation will focus on network communication patterns, protocols, DNS activity, application-layer traffic where available, potential indicators of compromise, and behavior that may be relevant to Cyber Threat Intelligence analysis.

## 2. Dataset

The selected PCAP is part of the CTU-IDSEVAL-6 dataset published by the Stratosphere Laboratory at Czech Technical University in Prague.

The dataset classifies this capture as malicious malware traffic. This classification provides context for the investigation but does not by itself constitute an analytical finding.

The analysis in this project will independently examine the network evidence contained in the PCAP.

## 3. Initial PCAP Metadata

The selected capture contains:

- 146,426 packets
- 15 MB file size
- 13 MB captured data
- Ethernet encapsulation
- Microsecond timestamp precision
- One capture interface
- Strict packet timestamp ordering

SHA256:

`ef51a29f19923e57ebb30cbe072e097c1136d940cf263a8e3ccb2deaf632f682`

## 4. Initial Metadata Observations

The PCAP timestamps range from 1970-01-01 to 1970-01-06.

These timestamps will not be interpreted as real-world calendar dates. Relative timing and packet ordering will instead be used when constructing the investigation timeline.

## 5. Investigation Methodology

The investigation will use:

- Wireshark for interactive packet-level analysis
- TShark for command-line packet extraction and filtering
- Zeek for structured network logs
- Python for selected data processing and analysis
- MITRE ATT&CK for behavioral mapping where supported by evidence

Further observations will be added as the investigation progresses.
