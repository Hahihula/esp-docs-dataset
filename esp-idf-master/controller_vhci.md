---
original_file_path: api-reference/bluetooth/controller_vhci.rst
---

# Controller & HCI

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

::::: only
esp32 or esp32c3 or esp32s3

## Application Examples

::: only
esp32

- `bluetooth/hci/ble_adv_scan_combined`{.interpreted-text role="example"} demonstrates how to use Bluetooth capabilities for advertising and scanning with a virtual Host Controller Interface (HCI). This example shows how to implement some host functionalities without a host and displays scanned advertising reports from other devices.
- `bluetooth/hci/controller_hci_uart_esp32`{.interpreted-text role="example"} demonstrates how to configure the Bluetooth LE Controller\'s HCI to communicate over UART on {IDF_TARGET_NAME}, enabling communication with an external Bluetooth host stack.
- `bluetooth/hci/controller_vhci_ble_adv`{.interpreted-text role="example"} demonstrates how to use the ESP-IDF VHCI ble_advertising app to perform advertising without a host and display received HCI events from the controller.
:::

::: only
esp32c3 or esp32s3

- `bluetooth/hci/controller_hci_uart_esp32c3_and_esp32s3`{.interpreted-text role="example"} demonstrates how to configure the Bluetooth LE Controller\'s HCI to communicate over UART on {IDF_TARGET_NAME}, enabling communication with an external Bluetooth host stack.
:::
:::::

## API Reference

::: include-build-file
inc/esp_bt.inc
:::

## HCI Vendor-specific (VS) Commands

Espressif\'s HCI VS commands are exclusively designed for use with Espressif\'s Bluetooth Host stack or internal debugging purposes. Application developers **should not** initialize or invoke these VS commands in their applications. Please refer to `bt_vhci`{.interpreted-text role="doc"} for detailed information.
