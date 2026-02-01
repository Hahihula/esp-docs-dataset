---
original_file_path: api-reference/bluetooth/esp_hf_defs.rst
---

# Bluetooth® HFP Defines

## Overview

This file contains definitions for constants, enumerations, and structures used in the Bluetooth Hands-Free Profile (HFP), enabling features like call management, audio control, and network status reporting.

## Application Examples

- `bluetooth/bluedroid/classic_bt/hfp_hf`{.interpreted-text role="example"} demonstrates how to use the Hands-Free Client Component to communicate with a device that implements Hands-Free Audio Gateway (HF-AG), such as a smartphone.
- `bluetooth/bluedroid/classic_bt/hfp_ag`{.interpreted-text role="example"} demonstrates how to use the Hands-Free Audio Gateway (HF-AG) component to communicate with a device that implements Hands-Free Client Role, such as a headphone set. It provides commands for configuring the project, establishing connections, controlling volume, and answering or rejecting calls.

## API Reference

::: include-build-file
inc/esp_hf_defs.inc
:::
