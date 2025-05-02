# NI-Switch Control Relay

This is a measurement plug-in example that controls relays using an NI relay
driver (e.g. PXI-2567).

## Features

- Uses the `custom_grpc_ni_switch_driver` APIs to access and control NI-SWITCH
  hardware from LabVIEW.
- Pin-aware, supporting one session and one pin.
  - Performs the same operation (open/close relay) on all selected pin/site
    combinations.
- Includes InstrumentStudio project files.
- Includes a TestStand sequence showing how to configure the pin map, register
  instrument sessions with the session management service, and run a
  measurement.
  - For the sake of simplicity, the TestStand sequence handles pin map and
    session registration and unregistration in the `Setup` and `Cleanup`
    sections of the main sequence. For **Test UUTs** and batch process model use
    cases, these steps should be moved to the `ProcessSetup` and
    `ProcessCleanup` callbacks.
- Uses the NI gRPC Device Server to allow sharing instrument sessions with other
  measurement services when running measurements from TestStand.

## Required Software

- InstrumentStudio 2025 Q1 or later
- TestStand 2024 Q4 or later
- NI-SWITCH driver 2024 Q4 or later
- custom_grpc_ni_switch_driver 1.0.0.2 or later

## Required Hardware

This example requires an NI relay driver (e.g. PXI-2567).

To simulate an NI SCOPE in software: open `NI MAX`, right click `Devices and
Interfaces` and select `Create New...`. Select `Simulated NI-DAQmx Device or
Modular Instrument`and click `Finish`. Search for and select the device you want
to simulate and click `OK`. Finally, click on the device and rename it to match
the name in the pin map file (e.g. RelayDriver1).
