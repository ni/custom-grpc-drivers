# Contributing to Custom gRPC Drivers

Contributions to Custom gRPC Drivers are welcome from all!

Custom gRPC Drivers is managed via [git](https://git-scm.com), with the canonical upstream
repository hosted on [GitHub](https://github.com/ni/custom-grpc-drivers).

Custom gRPC Drivers follows a pull-request model for development.  If you wish to
contribute, you will need to create a GitHub account, fork this project, push a
branch with your changes to your project, and then submit a pull request.

Please remember to sign off your commits (e.g., by using `git commit -s` if you
are using the command line client). This amends your git commit message with a line
of the form `Signed-off-by: Name Lastname <name.lastmail@emailaddress.com>`. Please
include all authors of any given commit into the commit message with a
`Signed-off-by` line. This indicates that you have read and signed the Developer
Certificate of Origin (see below) and are able to legally submit your code to
this repository.

See [GitHub's official documentation](https://help.github.com/articles/using-pull-requests/) for more details.

# Getting Started

This repo contains source code, package build specifications for building the source into VI packages, and examples showing how to write and run measurement plug-ins with custom gRPC drivers.

The source code can be found under the `Source` directory. The package definition files (.vipb) can be found under the `Build Specs` directory. The example code can be found under the `Examples` directory.

## Building the LabVIEW Packages

The source code is built into three LabVIEW packages

* `custom_grpc_drivers`
* `custom_grpc_ni_switch_driver`
* `custom_grpc_ni_daqmx_driver`

To build the packages:

1. Open the desired VIPM specification file (.vipb) under the [`Build Specs`](https://github.com/ni/custom-grpc-drivers/tree/main/Build%20Specs) folder
2. Open the Specification file using VIPM 2023 or later
3. Click Build - A .vip will be created in the `Build Output` folder under the repo root directory

## `custom_grpc_drivers` Package

The `custom_grpc_drivers` package contains the common LabVIEW menu (.mnu) files required for deploying the custom gRPC driver wrappers in the LabVIEW Functions palette.

## `custom_grpc_ni_switch_driver` Package

The `custom_grpc_ni_switch_driver` package contains the libraries needed for NI-Switch custom gRPC driver.

## `custom_grpc_ni_daqmx_driver` Package

The `custom_grpc_ni_daqmx_driver` package contains the libraries needed for NI-DAQmx custom gRPC driver.

## Examples

This repo contains example measurement services that show how to use the custom gRPC Drive API with NI hardware. For additional details on examples, please refer to the [example documentation](Examples/README.md).

# Developer Certificate of Origin (DCO)

   Developer's Certificate of Origin 1.1

   By making a contribution to this project, I certify that:

   (a) The contribution was created in whole or in part by me and I
       have the right to submit it under the open source license
       indicated in the file; or

   (b) The contribution is based upon previous work that, to the best
       of my knowledge, is covered under an appropriate open source
       license and I have the right under that license to submit that
       work with modifications, whether created in whole or in part
       by me, under the same open source license (unless I am
       permitted to submit under a different license), as indicated
       in the file; or

   (c) The contribution was provided directly to me by some other
       person who certified (a), (b) or (c) and I have not modified
       it.

   (d) I understand and agree that this project and the contribution
       are public and that a record of the contribution (including all
       personal information I submit with it, including my sign-off) is
       maintained indefinitely and may be redistributed consistent with
       this project or the open source license(s) involved.

(taken from [developercertificate.org](https://developercertificate.org/))

See [LICENSE](https://github.com/ni/custom-grpc-drivers/blob/main/LICENSE)
for details about how Custom gRPC Drivers is licensed.
