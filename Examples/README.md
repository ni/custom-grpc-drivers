# Examples

This directory contains the following example measurements:

- `NI-Switch Control Relay`: Demonstrates the controlling of relays using an NI relay driver (e.g. PXI-2567).
- `NI-DAQmx Measurement`: Demonstrates how to measure a finite single frequency sample using an NI DAQmx (e.g. PXIe-6621).

For more details about a specific example, see the `README.md` file included
with the example.

## User Guide

### Run the Measurement Service

To run the example measurement, follow these steps

1. Open the LabVIEW project (.lvproj) file for the example.
2. Each example includes a packed library for the LabVIEW UI. If you make any changes to `Measurement UI.vi`, rebuild the packed library build specification.
3. Open and Run the `Run Service.vi` VI to run the measurement service.
4. For examples that use a pin map, the name of the device in NI MAX must match
   the name of the device in the pin map.
5. For examples that have a TestStand sequence, the LabVIEW adapter
configuration must be set to use the LabVIEW development system. See the
[TestStand help](https://www.ni.com/docs/en-US/bundle/teststand-api-reference/page/tsref/labview-adapter-configuration-dialog-box.html) for more details.

### Stop the Measurement Service

Click the Stop button on the front panel of `Run Service.vi`.

## Developer Guide

### Make Changes to the Measurement Logic

Measurement logic for the measurements is contained in `Measurement Logic.vi`.

### How to add new UI elements

The User Interface is defined by `Measurement UI.vi`. The control and indicator
names in the User Interface should match the `Measurement Configuration` and
`Measurement Results`. If the datatype and name matches, then the data from the
UI will be sent to the logic before execution and the results will be published
to UI after the measurement is run.
