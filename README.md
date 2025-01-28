# PicoCmake
Cmake Template for Raspberry Pi Pico C Projects

# Raspberry Pi Pico C Project Template

This repository provides a template for developing C projects for the Raspberry Pi Pico using CMake and the Pico SDK because I am lazy and never can remember where pico_sdk_import is located within the SDK.

## Requirements

Following needs to be installed:

- **CMake** (version 3.13 or higher)
- **GNU Make** (I use Ninja because it has a cooler name)
- **Raspberry Pi Pico SDK**
- **ARM GCC Toolchain** for compiling C code for ARM architectures

### Setting up the Raspberry Pi Pico SDK

1. Clone the Raspberry Pi Pico SDK into your development environment:

   ```bash
   git clone https://github.com/raspberrypi/pico-sdk.git

2. Add environtment variable to the end of your .bashrc file

    ```bash
    export PICO_SDK_PATH=/path/to/pico-sdk