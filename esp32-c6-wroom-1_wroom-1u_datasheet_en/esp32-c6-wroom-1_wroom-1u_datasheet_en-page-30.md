Title: RF Characteristics

This section contains tables with RF characteristics of the Espressif product.

The RF data is measured at the antenna port, where RF cable is connected, including the front-end loss. The external antennas used for the tests on the modules with external antenna connectors have an impedance of 50 Ω.
Devices should operate in the center frequency range allocated by regional regulatory authorities. The target center frequency range and the target transmit power are configurable by software. See [ESP RF Test Tool](#) and [Test Guide](#) for instructions.

Unless otherwise stated, the RF tests are conducted with a 3.3 V (±5%) supply at 25 °C ambient temperature.

Subtitle: Wi-Fi Radio

Table Title: Table 7-1. Wi-Fi RF Characteristics
| Name | Description |
| --- | --- |
| Center frequency range of operating channel | 2412 ~ 2484 MHz |
| Wi-Fi wireless standard | IEEE 802.11b/g/n/ax |

Subtitle: Wi-Fi RF Transmitter (TX) Characteristics

Table Title: Table 7-2. TX Power with Spectral Mask and EVM Meeting 802.11 Standards
| Rate | Min (dBm) | Type | Max (dBm) |
| --- | --- | --- | --- |
| 802.11b, 1 Mbps, DSSS | — | - | **20.5** |
| 802.11b, 11 Mbps, CCK | — | - | **20.5** |
| 802.11g, 6 Mbps, OFDM | — | - | **20.0** |
| 802.11g, 54 Mbps, OFDM | — | - | **19.0** |
| 802.11n, HT20, MCS0 | — | - | **19.0** |
| 802.11n, HT20, MCS7 | — | - | **18.0** |
| 802.11n, HT40, MCS0 | — | - | **18.5** |
| 802.11n, HT40, MCS7 | — | - | **17.5** |
| 802.11ax, HE20, MCS0 | — | - | **19.0** |
| 802.11ax, HE20, MCS9 | — | - | **15.5** |

Table Title: Table 7-3. TX EVM Test^1
| Rate | Min (dB) | Type | Limit (dB) |
| --- | --- | --- | --- |
| 802.11b, 1 Mbps, DSSS | — | - | **−25.0** to **−10.0** |
| 802.11b, 11 Mbps, CCK | — | - | **−25.0** to **−10.0** |

Footer: Espressif Systems
Page Number and Document Information:
30 ESP32-C6-WROOM-1 & WROOM-1U Datasheet v1.4

Link Texts in the document:

- [ESP RF Test Tool](#)
- [Test Guide](#)

Note: The text "Cont'd on next page" indicates that there is additional content not shown here.

^1 Indicates continuation of Table 7-3 from a previous or subsequent section, as indicated by the superscript number.