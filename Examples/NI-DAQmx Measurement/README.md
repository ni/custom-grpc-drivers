# NI-DAQmx Measurement

This is a measurement plug-in example that demonstrates how to measure a finite single frequency sample using an NI DAQmx (e.g. PXIe-6612).

Specify values for Maximum and Minimum Measurement Time, CI Frequency Measurement Time and Read Timeout. The measured single frequency sample value will be displayed in the Data indicator.

## Features

- Uses the custom gRPC NI-DAQmx LabVIEW API
- Pin-aware, supporting one task and one pin
  - Uses the same selected measurement function and range for all selected pin/site combinations.
- Includes InstrumentStudio project files
- Includes a TestStand sequence showing how to configure the pin map, register
  instrument tasks with the session management service, and run a measurement.
  - For the sake of simplicity, the TestStand sequence handles pin map and task registration and unregistration in the `Setup` and `Cleanup` sections of the main sequence. For **Test UUTs** and batch process model use cases, these steps should be moved to the `ProcessSetup` and `ProcessCleanup` callbacks.
- Uses the NI gRPC Device Server to allow sharing instrument tasks with other
  measurement services when running measurements from TestStand

## Required Software

- [InstrumentStudio 2024 Q4](https://www.ni.com/en/support/downloads/software-products/download.instrumentstudio.html#549673) or later
- [TestStand 2021 SP1](https://www.ni.com/en/support/downloads/software-products/download.teststand.html#445937) or later
- [NI-DAQmx 2024 Q3.1](https://www.ni.com/en/support/downloads/drivers/download.ni-daq-mx.html#547031) or later
- [Measurement Plug-Ins SDK v.3.1.0.6](https://github.com/ni/measurement-plugin-labview/releases/tag/v3.1.0.6) or later
- [custom_grpc_ni_daqmx_driver 1.0.0.1](https://github.com/ni/custom-grpc-drivers/releases) or later

## Required Hardware

This example requires an NI DAQmx that is supported by NI-DAQmx (e.g. PXIe-6612).

To simulate an NI DAQmx in software: open `NI MAX`, right-click `Devices and Interfaces`,
select `Create New...`, and select `Simulated NI-DAQmx Device or Modular Instrument`.
DAQmx are in the `TIO Series (Counter Timer)` category.
