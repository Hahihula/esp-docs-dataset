---
original_file_path: api-guides/ble/ble-qualification.rst
---

# Bluetooth^®^ SIG Qualification

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

## Controller

The table below shows the latest qualification for Espressif Bluetooth LE Controller on each chip. For the qualification of Espressif modules, please check the [SIG Qualification Workspace](https://qualification.bluetooth.com/MyProjects/ListingsSearch).

+------------------------------------------------------------------------+-----------------------------------------------------------------------------------+-------------------+
| ::: centered                                                           | ::: centered                                                                      | ::: centered      |
| Chip Name                                                              | Design Number /                                                                   | Specification     |
| :::                                                                    | :::                                                                               | :::               |
|                                                                        |                                                                                   |                   |
|                                                                        | ::: centered                                                                      | ::: centered      |
|                                                                        | Qualified Design ID[^1]                                                           | Version[^2]       |
|                                                                        | :::                                                                               | :::               |
+========================================================================+===================================================================================+===================+
| ESP32                                                                  | .. centered:: [141661](https://qualification.bluetooth.com/ListingDetails/98048)  | .. centered:: 5.0 |
|                                                                        |                                                                                   |                   |
| (Bluetooth LE Mode)                                                    |                                                                                   |                   |
+------------------------------------------------------------------------+-----------------------------------------------------------------------------------+-------------------+
| ESP32                                                                  | .. centered:: [147845](https://qualification.bluetooth.com/ListingDetails/105426) | .. centered:: 4.2 |
|                                                                        |                                                                                   |                   |
| (Dual Mode: Bluetooth Classic & Bluetooth LE)                          |                                                                                   |                   |
+------------------------------------------------------------------------+-----------------------------------------------------------------------------------+-------------------+
| ESP32-C2 (ESP8684)                                                     | ::: centered                                                                      | ::: centered      |
|                                                                        | [194009](https://qualification.bluetooth.com/ListingDetails/160725)               | 5.3               |
|                                                                        | :::                                                                               | :::               |
+------------------------------------------------------------------------+-----------------------------------------------------------------------------------+-------------------+
| ESP32-C3                                                               | ::: centered                                                                      | ::: centered      |
|                                                                        | [239440](https://qualification.bluetooth.com/ListingDetails/212759)               | 5.4               |
|                                                                        | :::                                                                               | :::               |
+------------------------------------------------------------------------+-----------------------------------------------------------------------------------+-------------------+
| ESP32-C5                                                               | ::: centered                                                                      | ::: centered      |
|                                                                        | [Q331318](https://qualification.bluetooth.com/ListingDetails/257081)              | 6.0               |
|                                                                        | :::                                                                               | :::               |
+------------------------------------------------------------------------+-----------------------------------------------------------------------------------+-------------------+
| ESP32-C6                                                               | ::: centered                                                                      | ::: centered      |
|                                                                        | [Q335877](https://qualification.bluetooth.com/ListingDetails/262779)              | 6.0               |
|                                                                        | :::                                                                               | :::               |
+------------------------------------------------------------------------+-----------------------------------------------------------------------------------+-------------------+
| ESP32-C61                                                              | ::: centered                                                                      | ::: centered      |
|                                                                        | [Q331318](https://qualification.bluetooth.com/ListingDetails/257081)              | 6.0               |
|                                                                        | :::                                                                               | :::               |
+------------------------------------------------------------------------+-----------------------------------------------------------------------------------+-------------------+
| ESP32-S3                                                               | ::: centered                                                                      | ::: centered      |
|                                                                        | [239440](https://qualification.bluetooth.com/ListingDetails/212759)               | 5.4               |
|                                                                        | :::                                                                               | :::               |
+------------------------------------------------------------------------+-----------------------------------------------------------------------------------+-------------------+
| ESP32-H2                                                               | ::: centered                                                                      | ::: centered      |
|                                                                        | [Q331318](https://qualification.bluetooth.com/ListingDetails/257081)              | 6.0               |
|                                                                        | :::                                                                               | :::               |
+------------------------------------------------------------------------+-----------------------------------------------------------------------------------+-------------------+

## Host

The table below shows the latest qualification for Espressif Bluetooth LE Host.

+---------------+----------------------------------------------------------------------+---------------------------+
| ::: centered  | ::: centered                                                         | ::: centered              |
| Host          | Design Number / Qualified Design ID[^3]                              | Specification Version[^4] |
| :::           | :::                                                                  | :::                       |
+===============+======================================================================+===========================+
| ESP-Bluedroid | ::: centered                                                         | ::: centered              |
|               | [198312](https://qualification.bluetooth.com/ListingDetails/165785)  | 5.3                       |
|               | :::                                                                  | :::                       |
+---------------+----------------------------------------------------------------------+---------------------------+
| ESP-NimBLE    | ::: centered                                                         | ::: centered              |
|               | [Q371597](https://qualification.bluetooth.com/ListingDetails/310315) | 6.1                       |
|               | :::                                                                  | :::                       |
+---------------+----------------------------------------------------------------------+---------------------------+

[^1]: Since 1 July 2024, the identifying number for a new qualified design has changed from Qualified Design ID (QDID) to [Design Number (DN)](https://qualification.support.bluetooth.com/hc/en-us/articles/26704417298573-What-do-I-need-to-know-about-the-new-Qualification-Program-Reference-Document-QPRD-v3#:~:text=The%20identifying%20number%20for%20a%20Design%20has%20changed%20from%20Qualified%20Design%20ID%20(QDID)%20to%20Design%20Number%20(DN)). Please log in to the [Bluetooth SIG website](https://www.bluetooth.com/) to view Qualified Product Details, such as Design Details, TCRL Version, and ICS Details (passed cases) and etc.

[^2]: Some features of the Bluetooth Core Specification are optional. Therefore, passing the certification for a specific specification version does not necessarily mean supporting all the features specified in that version. Please refer to `Major Feature Support Status <ble-feature-support-status>`{.interpreted-text role="doc"} for the supported Bluetooth LE features on each chip.

[^3]: Since 1 July 2024, the identifying number for a new qualified design has changed from Qualified Design ID (QDID) to [Design Number (DN)](https://qualification.support.bluetooth.com/hc/en-us/articles/26704417298573-What-do-I-need-to-know-about-the-new-Qualification-Program-Reference-Document-QPRD-v3#:~:text=The%20identifying%20number%20for%20a%20Design%20has%20changed%20from%20Qualified%20Design%20ID%20(QDID)%20to%20Design%20Number%20(DN)). Please log in to the [Bluetooth SIG website](https://www.bluetooth.com/) to view Qualified Product Details, such as Design Details, TCRL Version, and ICS Details (passed cases) and etc.

[^4]: Some features of the Bluetooth Core Specification are optional. Therefore, passing the certification for a specific specification version does not necessarily mean supporting all the features specified in that version. Please refer to `Major Feature Support Status <ble-feature-support-status>`{.interpreted-text role="doc"} for the supported Bluetooth LE features on each chip.
