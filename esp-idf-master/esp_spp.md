---
original_file_path: api-reference/bluetooth/esp_spp.rst
---

# Bluetooth® SPP API

## Overview

SPP (Serial Port Profile) enables serial communication between Bluetooth devices, allowing them to exchange data over a virtual serial link. SPP API provides functionality to create both SPP initiators (clients) and acceptors (servers), enabling operation under different security requirements.

## Application Examples

- `bluetooth/bluedroid/classic_bt/bt_spp_acceptor`{.interpreted-text role="example"} demonstrates how to use Bluetooth capabilities to create a Serial Port Protocol (SPP) acceptor that acts as a server and integrate Secure Simple Pairing (SSP). This example also includes a demo for communicating with an SPP initiator that acts as a client.
- `bluetooth/bluedroid/classic_bt/bt_spp_initiator`{.interpreted-text role="example"} demonstrates how to use Bluetooth capabilities to create an SPP initiator that performs as a client and integrate SSP. This example also includes a demo for communicating with an SPP acceptor that acts as a server.
- `bluetooth/bluedroid/classic_bt/bt_spp_vfs_initiator`{.interpreted-text role="example"} demonstrates how to use SPP APIs to create an SPP initiator that acts as a client and communicates with an SPP acceptor, using Virtual File System (VFS) interface to send and receive data.

## API Reference

::: include-build-file
inc/esp_spp_api.inc
:::
