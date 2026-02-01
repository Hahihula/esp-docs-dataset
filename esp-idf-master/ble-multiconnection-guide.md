---
original_file_path: api-guides/ble/ble-multiconnection-guide.rst
---

# Multi-Connection Guide

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

## Introduction

The following table provides an overview of the maximum number of concurrent connections supported for each ESP Bluetooth LE Host. In multi-connection scenarios, connection parameters must be configured appropriately. In general, as the number of connections increases, the connection interval should be increased accordingly. For detailed parameter configuration recommendations and SDK configuration details, please refer to the corresponding example code in the following table.

In this document, the maximum number of connections refers to the maximum number of simultaneous active connections that the device can maintain, whether operating as a central or peripheral.

### Host SDKconfig

+---------------+--------------------+------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------+
| > Host        | Max Connections    | > SDKconfig                                                                                    | > Example                                                                               |
+===============+====================+================================================================================================+=========================================================================================+
| ESP-Bluedroid | 50                 | `BT_MULTI_CONNECTION_ENBALE <CONFIG_BT_MULTI_CONNECTION_ENBALE>`{.interpreted-text role="ref"} | `multi_conn <bluetooth/bluedroid/ble/ble_multi_conn>`{.interpreted-text role="example"} |
|               |                    |                                                                                                |                                                                                         |
|               |                    | `BT_ACL_CONNECTIONS <CONFIG_BT_ACL_CONNECTIONS>`{.interpreted-text role="ref"}                 |                                                                                         |
+---------------+--------------------+------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------+
| ESP-NimBLE    | 70                 | > `BT_NIMBLE_MAX_CONNECTIONS <CONFIG_BT_NIMBLE_MAX_CONNECTIONS>`{.interpreted-text role="ref"} | > `multi_conn<bluetooth/nimble/ble_multi_conn>`{.interpreted-text role="example"}       |
+---------------+--------------------+------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------+

: Maximum Concurrent Connections by ESP Bluetooth LE Host

### Controller SDKconfig

::: only
esp32

- `BTDM_CTRL_BLE_MAX_CONN <CONFIG_BTDM_CTRL_BLE_MAX_CONN>`{.interpreted-text role="ref"}

The configuration option **BTDM_CTRL_BLE_MAX_CONN** specifies the maximum number of Bluetooth LE connections that the controller can support concurrently. This value must match the maximum number of connections configured on the Host side, as defined in the table above.
:::

::: only
esp32c3 or esp32s3

- `BT_CTRL_BLE_MAX_ACT <CONFIG_BT_CTRL_BLE_MAX_ACT>`{.interpreted-text role="ref"}

The configuration option **BT_CTRL_BLE_MAX_ACT** defines the maximum number of Bluetooth LE activities that the controller can handle simultaneously. Each Bluetooth LE activity consumes one resource, including:

- Connections
- Advertising
- Scanning
- Periodic sync

Therefore, this parameter should be configured as follows:

**Maximum connections + required advertising, scanning and periodic sync instances**

**Example:** If the Host supports up to 8 connections, and the application requires 1 advertising instance and 1 scanning instance concurrently, set **BT_CTRL_BLE_MAX_ACT** to 10 (8 + 1 + 1).
:::

::: only
not esp32 and not esp32c3 and not esp32s3

- No controller-related SDK configuration is required.
:::

## Note

1.  The ability to support multiple connections highly depends on the application's overall memory usage. It is recommended to disable unnecessary features to optimize multi-connection performance.
2.  When the device operates in the peripheral role, connection stability and overall performance will be influenced by the central device and the negotiated connection parameters.

::: only
not esp32 and not esp32c3 and not esp32s3 and not esp32c2

3.  Due to the relatively higher memory usage of ESP-Bluedroid, it supports fewer concurrent connections compared to ESP-Nimble.
4.  If your application requires more simultaneous connections than the values listed above, please contact our [customer support team](https://www.espressif.com/en/contact-us/sales-questions) for further assistance.
:::

::: only
esp32 or esp32c3 or esp32s3
:::

::: only
esp32c2
:::

::: only
esp32h2
:::

::: only
esp32c6 or esp32c5 or esp32c61
:::
