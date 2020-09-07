# ddcset

[![travis-badge][]][travis] [![release-badge][]][release] [![license-badge][]][license]

`ddcset` is an application for controlling connected monitors over DDC/CI.

_Note: This fork was created to set up builds and provide a more recent version._


## Platforms

Currently supported platforms:

- Linux
  - `i2c-dev`: requires a supported graphics driver, and `modprobe i2c-dev`
    - Modern and open source drivers should support this. Older proprietary
      drivers such as fglrx may not work.
    - [NVIDIA GPUs will require additional configuration to work](#nvidia-drivers-on-linux).
- Windows
  - Windows Monitor Configuration API provides limited DDC/CI support on all GPUs.
  - NVIDIA NVAPI provides improved DDC/CI support for supported GPUs.

## Installation

[Binaries are available on some platforms](https://github.com/lgo/ddcset-rs/releases).
[Cargo](https://www.rust-lang.org/en-US/install.html) can also be used to install
directly from source:

    cargo install --force ddcset


## NVIDIA drivers on Linux

The NVIDIA Linux drivers have had broken DDC/CI support for years now. [There are
workarounds](http://www.ddcutil.com/nvidia/) but it seems that it is not
currently possible to use DDC/CI over DisplayPort.

[travis-badge]: https://img.shields.io/travis/lgo/ddcset-rs/master.svg?style=flat-square
[travis]: https://travis-ci.org/github/lgo/ddcset-rs
[release-badge]: https://img.shields.io/github/v/release/lgo/ddcset-rs.svg
[release]: https://github.com/lgo/ddcset-rs/releases
[license-badge]: https://img.shields.io/badge/license-MIT-ff69b4.svg?style=flat-square
[license]: https://github.com/arcnmx/ddcset-rs/blob/master/COPYING
