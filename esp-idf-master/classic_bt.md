---
original_file_path: api-reference/bluetooth/classic_bt.rst
---

# Bluetooth^®^ Classic

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

**Bluetooth Classic** provides APIs for implementing traditional Bluetooth functionalities, including audio streaming, device communication, and data exchange over the Serial Port Profile. It supports multiple Bluetooth profiles, allowing ESP devices to act as source or sink in scenarios like wireless audio, remote control, and data transmission.

The Bluetooth Classic API provides the following main features:

- Core protocol support (**GAP**, **L2CAP**, and **SDP**)
- Serial data communication (**SPP**)
- High-quality audio streaming (**A2DP**)
- Media playback control (**AVRCP**)
- Hands-free calling support (**HFP**)
- Input device connectivity (**HID** host and device roles)

------------------------------------------------------------------------

The Bluetooth Classic API in ESP-IDF is organized into the following parts:

**Core Protocols**

- `Bluetooth GAP <esp_gap_bt>`{.interpreted-text role="doc"}

  **Generic Access Profile (GAP):** Device discovery, pairing, and security management

- `Bluetooth L2CAP <esp_l2cap_bt>`{.interpreted-text role="doc"}

  **Logical Link Control and Adaptation Protocol (L2CAP):** Data multiplexing and channel management

- `Bluetooth SDP <esp_sdp>`{.interpreted-text role="doc"}

  **Service Discovery Protocol (SDP):** Discovers remote device services and attributes

**Communication Profile**

- `Bluetooth SPP <esp_spp>`{.interpreted-text role="doc"}

  **Serial Port Profile (SPP):** Emulates a serial communication channel over Bluetooth for data exchange

**Audio and Media Profiles**

- `Bluetooth A2DP <esp_a2dp>`{.interpreted-text role="doc"}

  **Advanced Audio Distribution Profile (A2DP):** High-quality audio streaming (source and sink)

- `Bluetooth AVRCP <esp_avrc>`{.interpreted-text role="doc"}

  **Audio/Video Remote Control Profile (AVRCP):** Media playback control (play, pause, volume)

**Hands-Free Profile (HFP)**

- `Bluetooth HFP Define <esp_hf_defs>`{.interpreted-text role="doc"}: Core definitions shared by HFP roles
- `Bluetooth HFP Client <esp_hf_client>`{.interpreted-text role="doc"}: Implements the hands-free unit role (e.g., headset, car kit)
- `Bluetooth HFP AG <esp_hf_ag>`{.interpreted-text role="doc"}: Implements the audio gateway role (e.g., mobile phone)

**Human Interface Device (HID)**

- `Bluetooth HID Device <esp_hidd>`{.interpreted-text role="doc"}: Implements peripheral roles such as keyboard, mouse, or game controller
- `Bluetooth HID Host <esp_hidh>`{.interpreted-text role="doc"}: Implements the host role for connecting to remote HID devices

Each part typically includes an **Overview**, **Application Examples**, and **API Reference**, covering purpose, main functionality, sample usage, and detailed API documentation.

::: {.toctree maxdepth="1" hidden=""}
Bluetooth GAP \<esp_gap_bt\> Bluetooth L2CAP \<esp_l2cap_bt\> Bluetooth SDP \<esp_sdp\> Bluetooth SPP \<esp_spp\> Bluetooth A2DP \<esp_a2dp\> Bluetooth AVRCP \<esp_avrc\> Bluetooth HFP Define \<esp_hf_defs\> Bluetooth HFP Client \<esp_hf_client\> Bluetooth HFP AG \<esp_hf_ag\> Bluetooth HID Device \<esp_hidd\> Bluetooth HID Host \<esp_hidh\>
:::
