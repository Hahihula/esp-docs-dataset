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
| Wi-Fi wireless standard | IEEE 802.11b/g/n |

Subtitle: Wi-Fi RF Transmitter (TX) Characteristics

Table Title: Table 7-2. TX Power with Spectral Mask and EVM Meeting 802.11 Standards
| Rate | Min (dBm) | Typ (dBm) | Max (dBm) |
| --- | --- | --- | --- |
| 802.11b, 1 Mbps | — | 20.5 | — |
| 802.11b, 11 Mbps | — | 20.5 | — |
| 802.11g, 6 Mbps | — | 20.0 | — |
| 802.11g, 54 Mbps | — | 18.0 | — |
| 802.11n, HT20, MCS 0 | — | 19.0 | — |
| 802.11n, HT20, MCS 7 | — | 17.5 | — |
| 802.11n, HT40, MCS 0 | — | 18.5 | — |
| 802.11n, HT40, MCS 7 | — | 17.0 | — |

Table Title: Table 7-3. TX EVM Test^1
| Rate | Min (dB) | Typ (dB) | Limit (dB) |
| --- | --- | --- | --- |
| 802.11b, 1 Mbps, @20.5 dBm | — | -24.5 | -10 |
| 802.11b, 11 Mbps, @20.5 dBm | — | -24.5 | -10 |
| 802.11g, 6 Mbps, @20 dBm | — | -23.0 | -5 |
| 802.11g, 54 Mbps, @18 dBm | — | -29.5 | -25 |

Footer: Cont'd on next page

Page Number and Document Information:
- Page number at the bottom of each table is indicated as "33".
- At the very end (bottom right), there's a reference to document version or type, which reads: "ESP32-S3-MINI-1 & MINI-1U Datasheet v1.6".

[Note: The actual URLs and references are not provided in this transcription as they appear broken or incomplete.]