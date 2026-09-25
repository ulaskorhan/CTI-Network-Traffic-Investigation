# Dataset

## CTU-IDSEVAL-6

This project uses the CTU-IDSEVAL-6 dataset published by the Stratosphere Laboratory at the Czech Technical University in Prague.

Source:

https://zenodo.org/records/21027042

DOI:

10.5281/zenodo.21027042

## Dataset Description

CTU-IDSEVAL-6 is a labeled network traffic dataset designed for evaluating intrusion detection systems.

The dataset contains six network captures covering:

- One benign user traffic capture

- Two malware traffic captures

- Three port scan captures

The dataset provides:

- Raw PCAP network captures

- Zeek-derived network flow data

- Labels describing observed traffic

- Dataset documentation

The complete dataset contains approximately 1.1 million packets and 286,000 labeled network flows.

## Use in This Project

The raw PCAP data will be analyzed independently using Wireshark, TShark, Zeek and Python.

The supplied labels and Zeek data may be used as reference material during the investigation, but observations and assessments in this project will be based primarily on analysis of the network traffic.

## Investigation Scope

A specific capture will be selected from the dataset for detailed investigation.

The investigation will examine:

- Network hosts

- Connections

- Protocols

- DNS activity

- HTTP and TLS activity where available

- Communication patterns

- Potentially suspicious network behavior

- Indicators of Compromise

- Relevant MITRE ATT&CK techniques

## Dataset Limitations

The dataset is a controlled research dataset and should not be treated as representative of all real-world network environments.

The analysis will therefore distinguish between observed evidence, analytical assessment and uncertainty.

## Attribution

Dataset:

Garcia, Sebastian; Valeros, Veronica; Alya, Gomaa.

CTU-IDSEVAL-6: A Labeled Network Dataset for the Evaluation of Intrusion Detection Systems.

Czech Technical University in Prague, 2026.

DOI: 10.5281/zenodo.21027042


## Selected Capture

The investigation focuses on:

`ctu-idseval-6-malicious-malware-1.pcap`

### PCAP Metadata

| Property | Value |

|---|---|

| File type | Wireshark/tcpdump PCAP |

| Encapsulation | Ethernet |

| Number of packets | 146,426 |

| File size | 15 MB |

| Data size | 13 MB |

| Capture duration | 511,669.678382 seconds |

| Time precision | Microseconds |

| Interfaces | 1 |

| Strict time order | True |

| SHA256 | `ef51a29f19923e57ebb30cbe072e097c1136d940cf263a8e3ccb2deaf632f682` |

### Timestamp Note

The earliest packet timestamp is recorded as `1970-01-01 01:00:00.000015` and the latest as `1970-01-06 23:07:49.678397`.

These timestamps are treated as dataset capture timestamps rather than interpreted as meaningful real-world calendar dates. Relative timing and ordering will be used when developing the investigation timeline.
