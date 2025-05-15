# Custom gRPC Drivers

- [Custom gRPC Drivers](#custom-grpc-drivers)
  - [Introduction](#introduction)
  - [Software support](#software-support)
  - [Installation](#installation)
  - [Workflow](#workflow)
  - [Using the Custom gRPC Drivers](#using-the-custom-grpc-drivers)
  - [Examples](#examples)

---

## Introduction

The Custom gRPC Drivers package offers NI gRPC Device Server interface APIs in LabVIEW. These APIs facilitate efficient communication between LabVIEW applications and hardware devices using the gRPC protocol, enabling session sharing across LabVIEW Measurement Plug-ins.

## Software support

- [InstrumentStudio 2024 Q4](https://www.ni.com/en/support/downloads/software-products/download.instrumentstudio.html#549673) or later
- [LabVIEW 2021 SP1](https://www.ni.com/en/support/downloads/software-products/download.labview.html#487445) or later
  - [JKI VI Package Manager 2021 SP1](https://www.ni.com/en/support/downloads/tools-network/download.jki-vi-package-manager.html#443251) or later
    - [Measurement Plug-In SDK v3.1.0.6](https://www.ni.com/docs/en-US/bundle/measurementplugins/page/labview-measurement-dependencies.html) or later
    - [LabVIEW gRPC Library v1.3.0.1](https://www.vipm.io/package/ni_lib_labview_grpc_library/#1.3.0.1) or later
    - [LabVIEW gRPC Servicer v1.3.0.1](https://www.vipm.io/package/ni_lib_labview_grpc_servicer/#1.3.0.1) or later
    - [NI gRPC Types v1.0.0.1](https://www.vipm.io/package/ni_protobuf_types/#1.0.0.1) or later
- [TestStand 2021 SP1](https://www.ni.com/en/support/downloads/software-products/download.teststand.html#445937) or later

---

## Supported Instruments

1. NI-Switch
2. NI-DAQmx 

## Supported APIs and Property Nodes

### NI-Switch

|#| **Function Name**             | 
|-| ----------------------------- |
|1| `Initialize With Topology.vi` | 
|2| `Relay Control.vi`            | 
|3| `Get Relay Position.vi`       | 
|4| `Wait For Debounce.vi`        | 
|5| `Close.vi`                    | 

### NI-DAQmx

|#| **Function Name**            
|-| ----------------------------- 
|1| `DAQmx Create Task.vi`
|2| `DAQmx Create Channel (DO-Digital Output).vi`
|3| `DAQmx Create Channel (CI-Frequency).vi `
|4| `DAQmx Write (Digital Bool 1Line 1Point).vi` 
|5| `DAQmx Read (Counter DBL 1Chan 1Samp).vi`     
|6| `DAQmx Timing (Implicit).vi`             
|7| `DAQmx Start Task.vi`                       
|8| `DAQmx Stop Task.vi` 
|9| `DAQmx Clear Task.vi`

|#| **Property Node**            
|-| ----------------------------- 
|1| `DAQmx Task >> Name`
|2|`DAQmx Channel >> Counter Input : Frequency : Input : Terminal`         
|3| `DAQmx Channel >> Counter Input : Frequency : Measurement Specifications : High Frequency : Measurement Time` 

---

## Installation

1. Install the latest [Custom gRPC Driver Packages](https://github.com/ni/custom-grpc-drivers/releases) in VIPM.

---

## Workflow

![Workflow](Docs/Images/Design_Flow.png)

---

## Using the Custom gRPC Drivers

1. Open the Block Diagram of your application (or) Create and save a new VI.
2. Right-click on the Block Diagram and navigate to `Measurement I/O` → `Custom gRPC Drivers` to use the Custom gRPC Driver APIs.  
![Custom gRPC Driver Palette](Docs/Images/Custom%20gRPC%20Driver%20Palette.png)

---

## Examples

The `Examples` directory contains example measurement services. See the [README.md](Examples/README.md) file for more information.

---

> [!NOTE]
> For detailed information about the Custom gRPC Drivers available in this repository, please refer to the documentation located in the [Docs](Docs) directory.
