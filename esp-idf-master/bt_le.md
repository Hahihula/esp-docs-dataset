---
original_file_path: api-reference/bluetooth/bt_le.rst
---

# Bluetooth^®^ Low Energy

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

**Bluetooth Low Energy (Bluetooth LE)** provides low-power wireless communication for IoT devices such as wearables, sensors, and smart home products. This section documents the **Bluetooth LE API Reference**, covering APIs for device discovery, data exchange, and Wi-Fi provisioning over Bluetooth LE.

For usage concepts and tutorials, see `Bluetooth Low Energy <../../../api-guides/ble/index>`{.interpreted-text role="doc"} in **API Guides**.

The Bluetooth LE API in ESP-IDF is organized into the following parts:

- `Bluetooth Low Energy GAP <esp_gap_ble>`{.interpreted-text role="doc"}

  Handles advertising, scanning, connection management, and security operations

- `Bluetooth Low Energy GATT Define <esp_gatt_defs>`{.interpreted-text role="doc"}

  Common data types and constants for attributes, characteristics, and UUIDs used in GATT operations

- `Bluetooth Low Energy GATT Server <esp_gatts>`{.interpreted-text role="doc"}

  Exposes services and characteristics to remote clients (peripheral role)

- `Bluetooth Low Energy GATT Client <esp_gattc>`{.interpreted-text role="doc"}

  Discovers and accesses services on remote servers (central role)

::: only
SOC_BLUFI_SUPPORTED

- `Bluetooth Low Energy BluFi <esp_blufi>`{.interpreted-text role="doc"}

  Enables Wi-Fi provisioning and configuration via Bluetooth LE
:::

Each part typically includes an **Overview**, **Application Examples**, and **API Reference**, covering purpose, main functionality, sample usage, and detailed API documentation.

::: {.toctree maxdepth="1" hidden=""}
Bluetooth Low Energy GAP \<esp_gap_ble\> Bluetooth Low Energy GATT Define \<esp_gatt_defs\> Bluetooth Low Energy GATT Server \<esp_gatts\> Bluetooth Low Energy GATT Client \<esp_gattc\> :SOC_BLUFI_SUPPORTED: Bluetooth Low Energy BluFi \<esp_blufi\>
:::
