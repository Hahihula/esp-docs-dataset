Title: RF Characteristics

This section contains tables with RF characteristics of the Espressif product.

The RF data is measured at the antenna port, where RF cable is connected, including the front-end loss.
Devices should operate in the center frequency range allocated by regional regulatory authorities. The target center frequency range and the target transmit power are configurable by software. See [ESP RF Test Tool](#) and [Test Guide](#) for instructions.

Unless otherwise stated, the RF tests are conducted with a 3.3 V (±5%) supply at 25 °C ambient temperature.

Subtitle: 7.1 2.4 GHz Wi-Fi Radio

Table Title: Table 7-1, 2.4 GHz Wi-Fi RF Characteristics
| Name | Description |
| --- | --- |
| Center frequency range of operating channel | 2412 ~ 2484 MHz |
| Wi-Fi wireless standard | IEEE 802.11b/g/n/ax |

Subtitle: 7.1.1 2.4 GHz Wi-Fi RF Transmitter (TX) Characteristics

Table Title: Table 7-2, 2.4 GHz TX Power with Spectral Mask and EVM Meeting 802.11 Standards
| Rate | Min (dBm) | Type | Max (dBm) |
| --- | --- | --- | --- |
| 802.11b, 1 Mbps, DSSS | — | - | 19.5 |
| 802.11b, 11 Mbps, CCK | — | - | 19.5 |
| 802.11g, 6 Mbps, OFDM | — | - | 18.5 |
| 802.11g, 54 Mbps, OFDM | — | - | 16.5 |
| 802.11n, HT20, MCS0 | (dBm) | Type | Max (dBm) |
| --- | --- | --- | --- |
| 802.11n, HT20, MCS7 | — | - | 16.5 |
| 802.11n, HT40, MCS0 | — | - | 17.5 |
| 802.11n, HT40, MCS7 | (dBm) | Type | Max (dBm) |
| --- | --- | --- | --- |
| 802.11ax, HE20, MCS0 | — | - | 18.5 |
| 802.11ax, HE20, MCS9 | (dBm) | Type | Max (dBm) |
| --- | --- | --- | --- |

Table Title: Table 7-3, 2.4 GHz TX EVM Test
| Rate | Min (dB) | Typ (dB) | Limit (dB) |
| --- | --- | --- | --- |
| 802.11b, 1 Mbps, DSSS | — | - | −25.0 to −10.0 |
| 802.11b, 11 Mbps, CCK | (dB) | Type | Max (dBm) |
| --- | --- | --- | --- |
| 802.11g, 6 Mbps, OFDM | — | - | −22.0 to −5.0 |

Footer: Cont'd on next page

Company Information:
Espressif Systems
Page Number and Document Version Info: ESP32-C5-MINI-1 Datasheet v1.0 Submit Documentation Feedback