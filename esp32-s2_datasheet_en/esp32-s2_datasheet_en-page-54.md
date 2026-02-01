**Title:**
6 RF Characteristics

**Body Text:**
This section contains tables with RF characteristics of the Espressif product.

The RF data is measured at the antenna port, where RF cable is connected, including the front-end loss. The front-end circuit is a 0 Ω resistor.
Devices should operate in the center frequency range allocated by regional regulatory authorities. The target center frequency range and the target transmit power are configurable by software. See [ESP RF Test Tool](#) and [Test Guide](#) for instructions.

Unless otherwise stated, the RF tests are conducted with a 3.3 V (±5%) supply at 25 °C ambient temperature.

**Subtitle:**
6.1 Wi-Fi Radio

**Table Title: Table 6-1. Wi-Fi Frequency**

| Parameter | Min (MHz) | Typ (MHz) | Max (MHz) |
|-----------|-----------|-----------|-----------|
| Center frequency of operating channel | **2412** | — | **2484** |

**Subtitle:**
6.1.1 Wi-Fi RF Transmitter (TX) Characteristics

**Table Title: Table 6-2. TX Power with Spectral Mask and EVM Meeting 802.11 Standards**

| Rate | Min (dBm) | Typ (dBm) | Max (dBm) |
|------|-----------|-----------|-----------|
| 802.11b, 1 Mbps | — | **19.5** | — |
| 802.11b, 11 Mbps | — | **19.5** | — |
| 802.11g, 6 Mbps | — | **18.0** | — |
| 802.11g, 54 Mbps | — | **18.0** | — |
| 802.11n, HT20, MCS0 | — | **18.0** | — |
| 802.11n, HT20, MCS7 | — | **17.0** | — |
| 802.11n, HT40, MCS0 | — | **18.0** | — |
| 802.11n, HT40, MCS7 | — | **16.5** | — |

**Table Title: Table 6-3. TX EVM Test**

| Rate | Min (dB) | Typ (dB) | SL (dB) |
|------|----------|----------|---------|
| 802.11b, 1 Mbps, @19.5 dBm | — | **—25** | -10 |
| 802.11b, 11 Mbps, @19.5 dBm | — | **—25** | -10 |
| 802.11g, 6 Mbps, @18 dBm | — | **—28** | -5 |
| 802.11g, 54 Mbps, @18 dBm | — | **—28** | -5 |
| 802.11n, HT20, MCS0, @18 dBm | — | **—26** | -5 |

**Footer:**
Espressif Systems
Page number: 54

Submit Documentation Feedback ESP32-S2 Series Datasheet v1.8