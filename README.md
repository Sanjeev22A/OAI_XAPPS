---

# 🛰️ oai_Xapps

## Overview

This repository contains resources, flowcharts, and installation guides for setting up and understanding **OpenAirInterface (OAI)** and **FlexRIC** with Docker-based environments.
It is designed to help researchers, developers, and students build, visualize, and experiment with **xApps** integrated into the **O-RAN (Open RAN)** architecture using the OAI stack.

---

## 🔍 What is OpenAirInterface (OAI)?

**OpenAirInterface (OAI)** is an open-source project that implements the full 4G/5G RAN and Core Network.
It allows simulation, testing, and validation of 5G features such as:

* **gNB/eNB** implementations (RAN)
* **EPC/5GC** for core network functionality
* **PHY, MAC, RLC, PDCP** and higher layers
* **O-RAN-compliant interfaces** like **E2**, **A1**, and **F1**

OAI enables research and development of end-to-end 5G networks in both simulated and real hardware environments.

---

## ⚙️ What is OAI FlexRIC?

**FlexRIC** is a lightweight and modular **O-RAN-compliant RAN Intelligent Controller (RIC)** framework developed under OAI.
It enables integration of **xApps** and **rApps** to implement real-time and near-real-time control loops for RAN optimization.

### 🔧 Key Features:

* Implements the **E2 interface** for communication between gNB and near-RT RIC.
* Supports **E2AP**, **E2SM-KPM**, and **E2SM-RC** services.
* Provides APIs for xApp development and E2 agent management.
* Dockerized setup for simplified deployment and testing.

FlexRIC enables you to:

* Monitor 5G KPIs in real time.
* Develop custom xApps for resource management, scheduling, or anomaly detection.
* Integrate AI/ML modules for intelligent RAN control.

---

## 🐳 Running OAI FlexRIC in Docker

This repository is structured to support **Docker-based deployment** of the OAI and FlexRIC environment.

Typical workflow:

1. **Build and configure** OAI components inside Docker.
2. **Launch the RIC and E2 Agent containers** (gNB/UE).
3. **Develop and deploy xApps** that communicate with the near-RT RIC.
4. **Visualize data flows** using the flowcharts and protocol documents provided.

---

## 📁 Repository Structure

| Folder / File                        | Description                                                                                                  |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| **Flowchart/**                       | Contains flow diagrams and protocol-level data flow explanations for different layers (PHY, MAC, RLC, PDCP). |
| ┣ 📄 `F1 Interface.md`               | Explains the F1-C/F1-U interface flow between gNB and DU.                                                    |
| ┣ 📄 `MAC_LAYER_DATA_FLOW.md`        | Describes MAC-layer scheduling and data flow in OAI.                                                         |
| ┣ 📄 `PDCP_Functional_Flow_OAI.md`   | Functional overview of PDCP in OAI.                                                                          |
| ┣ 📄 `PHY_RF.md`                     | Details PHY and RF data flow.                                                                                |
| ┣ 📄 `Protocol_Flow_5G.md`           | Complete 5G protocol flow overview.                                                                          |
| ┣ 📄 `RLC Packet flow.md`            | Visualizes RLC layer packet handling.                                                                        |
| **OAI_Installation/**                | Contains installation and build instructions for OAI.                                                        |
| ┣ 📄 `Build_Options.md`              | Describes OAI build-time configuration options.                                                              |
| ┣ 📄 `Guide.md`                      | Step-by-step guide to install and configure OAI.                                                             |
| **OAI_Guide.pdf**                    | Comprehensive OAI setup and architecture documentation.                                                      |
| **OAI_INSTALLTION_SINGLEUE_MODE.md** | Explains how to run OAI in single-UE test mode.                                                              |
| **README.md**                        | (This file) Overview of the repository and usage instructions.                                               |

---

## 🧠 Suggested Use Cases

* **Learning**: Understand how different OAI layers interact (PHY → PDCP).
* **Research**: Develop and test xApps for PRB allocation, KPI monitoring, or traffic classification.
* **Development**: Prototype and deploy custom near-RT RIC functions in a Dockerized environment.
* **Simulation**: Run OAI-based gNB + UE with FlexRIC to emulate realistic network conditions.

---

## 📘 References

* [OAI Official Website](https://openairinterface.org/)
* [FlexRIC GitHub Repository](https://gitlab.eurecom.fr/mosaic5g/flexric)
* [O-RAN Alliance Specifications](https://www.o-ran.org/specifications)
* [OAI Documentation Portal](https://openairinterface.org/oai-documentation/)

---

