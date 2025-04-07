# Readme

## Introduction

This is simple example to close and open a relay using niSE with session management capabilities. Created a custom session management API's in folder `Sessions\niSE`.
`niSE simple relay - Connect\niSE simple connect.lvproj` is the plugin to connect the switch route, while `niSE simple relay - Disconnect\niSE simple disconnect.lvproj` is the plugin to disconnect the route.

## Prerequistes

1. A driver service is required to receive the session handling request. A example is available at [Language agnostic driver repository.](https://github.com/ni/multi-language-driver-support/tree/users/prem/reusable-niSE-driver-example).
2. Start the service before running the measurements.
3. A pinmap file is available in parallel to readme. This has the basic definition of the custom instrument for niSE.