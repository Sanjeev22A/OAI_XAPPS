---

#  OAI_Xapps

## Overview

This repository contains resources, flowcharts, and installation guides for setting up and understanding **OpenAirInterface (OAI)** and **FlexRIC** with Docker-based environments.
It is designed to help researchers, developers, and students build, visualize, and experiment with **xApps** integrated into the **O-RAN (Open RAN)** architecture using the OAI stack.

---

##  What is OpenAirInterface (OAI)?

**OpenAirInterface (OAI)** is an open-source project that implements the full 4G/5G RAN and Core Network.
It allows simulation, testing, and validation of 5G features such as:

* **gNB/eNB** implementations (RAN)
* **EPC/5GC** for core network functionality
* **PHY, MAC, RLC, PDCP** and higher layers
* **O-RAN-compliant interfaces** like **E2**, **A1**, and **F1**

OAI enables research and development of end-to-end 5G networks in both simulated and real hardware environments.

---

##  What is OAI FlexRIC?

**FlexRIC** is a lightweight and modular **O-RAN-compliant RAN Intelligent Controller (RIC)** framework developed under OAI.
It enables integration of **xApps** and **rApps** to implement real-time and near-real-time control loops for RAN optimization.

###  Key Features:

* Implements the **E2 interface** for communication between gNB and near-RT RIC.
* Supports **E2AP**, **E2SM-KPM**, and **E2SM-RC** services.
* Provides APIs for xApp development and E2 agent management.
* Dockerized setup for simplified deployment and testing.

FlexRIC enables you to:

* Monitor 5G KPIs in real time.
* Develop custom xApps for resource management, scheduling, or anomaly detection.
* Integrate AI/ML modules for intelligent RAN control.

---

##  Repository Structure

| Folder / File | Description |
|----------------|-------------|
| [**Flowchart/**](Flowchart/) | Contains flow diagrams and protocol-level data flow explanations for different layers (PHY, MAC, RLC, PDCP). |
| ┣ [F1 Interface.md](Flowchart/F1%20Interface.md) | Explains the F1-C/F1-U interface flow between gNB and DU. |
| ┣ [MAC_LAYER_DATA_FLOW.md](Flowchart/MAC_LAYER_DATA_FLOW.md) | Describes MAC-layer scheduling and data flow in OAI. |
| ┣ [PDCP_Functional_Flow_OAI.md](Flowchart/PDCP_Functional_Flow_OAI.md) | Functional overview of PDCP in OAI. |
| ┣ [PHY_RF.md](Flowchart/PHY_RF.md) | Details PHY and RF data flow. |
| ┣ [Protocol_Flow_5G.md](Flowchart/Protocol_Flow_5G.md) | Complete 5G protocol flow overview. |
| ┣ [RLC Packet flow.md](Flowchart/RLC%20Packet%20flow.md) | Visualizes RLC layer packet handling. |
| [**OAI_Installation/**](OAI_Installation/) | Contains installation and build instructions for OAI. |
| ┣ [Build_Options.md](OAI_Installation/Build_Options.md) | Describes OAI build-time configuration options. |
| ┣ [Guide.md](OAI_Installation/Guide.md) | Step-by-step guide to install and configure OAI. |
| ┣ [OAI_Guide.pdf](OAI_Installation/OAI_Guide.pdf) | Comprehensive OAI setup and architecture documentation. |
| [OAI_INSTALLTION_SINGLEUE_MONOLITHIC_GNB_NEAR_RT_RIC.md](OAI_INSTALLTION_SINGLEUE_MONOLITHIC_GNB_NEAR_RT_RIC.md) | Explains how to run OAI in single-UE test mode with a monolithic gNB architecture and Near-RT RIC support. |
| [README.md](README.md) | (This file) Overview of the repository and usage instructions. |

---

##  Suggested Use Cases

* **Learning**: Understand how different OAI layers interact (PHY → PDCP).
* **Research**: Develop and test xApps for PRB allocation, KPI monitoring, or traffic classification.
* **Development**: Prototype and deploy custom near-RT RIC functions in a Dockerized environment.
* **Simulation**: Run OAI-based gNB + UE with FlexRIC to emulate realistic network conditions.

---

##  References

* [OAI Official Website](https://openairinterface.org/)
* [FlexRIC GitHub Repository](https://gitlab.eurecom.fr/mosaic5g/flexric)
* [O-RAN Alliance Specifications](https://www.o-ran.org/specifications)
* [OAI Documentation Portal](https://openairinterface.org/oai-documentation/)

---
## Scopes To Look Into
* Kubernetes and Helm Integration into a deployable End to End Network
* Multi UE Setup
* GNB Split/ Disaggregation
