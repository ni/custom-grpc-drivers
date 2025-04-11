# gRPC DAQmx LabVIEW - Temporary Solution

- [gRPC DAQmx LabVIEW - Temporary Solution](#grpc-daqmx-labview---temporary-solution)
    - [Who](#who)
    - [Feature WorkItem](#feature-workitem)
    - [Problem Statement](#problem-statement)
        - [Key Requirements](#key-requirements)
    - [Session Management Workflow](#session-management-workflow)


## Who

- Author: National Instruments
- Team: _Interlligent Validation_

## Feature WorkItem

[Feature: gRPC DAQmx LabVIEW - temporary solution](https://dev.azure.com/ni/DevCentral/_workitems/edit/3055103/)

## Problem Statement

The NI DAQmx is not supported (as of Apr 2025) in terms of session management and reuse across LabVIEW Measurement Plug-in when used in InstrumentStudio or TestStand workflows. gRPC device server support is required to enable the workflows with IS Pro.

### Key Requirements

**gRPC Server:** Implement a gRPC server to support DAQmx functions and manage IS Pro session initialization behaviors.

**gRPC Client in LabVIEW:** Provide VIs for all gRPC server methods, ensuring connector pane matching and session management using class objects.

**TestStand:** Offer helper functions (VIs) for building automation sequences with the DAQmx gRPC driver.

**Examples:** Create LabVIEW and TestStand examples demonstrating DAQmx client usage and helper functions.

**Deployment:** Deploy the gRPC server and client VIs using NI and VI Packages, respectively.

## Session Management Workflow

