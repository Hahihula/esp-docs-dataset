---
original_file_path: api-reference/network/esp_smartconfig.rst
---

# SmartConfig

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

## Introduction

The SmartConfig^TM^ is a provisioning technology developed by TI to connect a new Wi-Fi device to a Wi-Fi network. It uses a mobile application to broadcast the network credentials from a smartphone, or a tablet, to an un-provisioned Wi-Fi device.

The advantage of this technology is that the device does not need to directly know SSID or password of an Access Point (AP). This information is provided using the smartphone. This is particularly important to headless device and systems, due to their lack of a user interface.

Currently, {IDF_TARGET_NAME} support three types of SmartConfig: Airkiss, ESPTouch, and ESPTouch v2. ESPTouch v2 has been supported since SmartConfig v3.0 (the version of SmartConfig can be get from `esp_smartconfig_get_version()`{.interpreted-text role="cpp:func"}), and it employs a completely different algorithm compared to ESPTouch, resulting in faster setup times. Additionally, ESPTouch v2 introduces AES encryption and custom data fields.

Starting from SmartConfig v3.0.2, ESPTouch v2 introduces support for random IV in AES encryption. On the application side, when the option for random IV is disabled, the default IV is set to 0, maintaining consistency with previous versions. When the random IV option is enabled, the IV will be a random value. It is important to note that when AES encryption is enabled with a random IV, the provision time will be extended due to the need of transmitting the IV to the provisioning device. On the provisioning device side, the device will identify whether the random IV for AES is enabled based on the flag in the provisioning packet.

If you are looking for other options to provision your {IDF_TARGET_NAME} devices, check `../provisioning/index`{.interpreted-text role="doc"}.

## Application Example

Connect {IDF_TARGET_NAME} to the target AP using SmartConfig: `wifi/smart_config`{.interpreted-text role="example"}.

## API Reference

::: include-build-file
inc/esp_smartconfig.inc
:::
