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

## 6. Candidate Network Indicator: 41.108.179.197

During the initial network analysis, repeated outbound TCP connection
attempts from internal host `192.168.1.115` to `41.108.179.197` on
destination port `1177/TCP` were identified.

### Observations

The observed traffic contains repeated TCP SYN packets originating from
`192.168.1.115`. The source port changes between connection attempts,
while the destination remains `41.108.179.197:1177`.

The activity occurs repeatedly over an extended period of the capture.
The observed attempts also show an approximately regular temporal pattern,
with intervals in the region of several seconds between some attempts.

This behavior is notable because it differs from the ordinary web
traffic observed from the same internal host, where HTTP requests,
responses, and application-layer data were observed.

### External Enrichment

The destination IP address was checked using VirusTotal. No useful
reputation or related intelligence was identified for the IP address.

Consequently, external reputation data does not currently provide
independent evidence that the destination is malicious.

### Related Network Evidence

An ICMP Redirect involving `192.168.1.2` and `192.168.1.115` was also
observed in connection with one of the packets. The ICMP message contained
the original TCP connection attempt to `41.108.179.197:1177`.

The ICMP Redirect was treated as routing-related network activity and
was not considered evidence of malicious behavior.

### Assessment

The repeated connection attempts to `41.108.179.197:1177`, including
their approximately periodic occurrence, represent an anomalous network
behavior that warrants further investigation.

At this stage, the available evidence is insufficient to independently
confirm that `41.108.179.197` is malicious or that the traffic
represents command and control activity.

The IP is therefore treated as a **candidate network indicator** rather
than a confirmed Indicator of Compromise.

### Confidence

**Moderate confidence** in the observation that repeated automated
connection attempts occurred.

**Low confidence** in any conclusion regarding the malicious nature or
purpose of the traffic based solely on the currently available evidence.

### Investigation Status

The indicator will be retained for correlation with other network,
DNS, host, and behavioral evidence during the remainder of the
investigation.

