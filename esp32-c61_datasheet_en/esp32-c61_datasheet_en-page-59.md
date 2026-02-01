**Title: RF Characteristics**

This section contains tables with RF characteristics of the Espressif product.

The RF data is measured at the antenna port, where RF cable is connected, including the front-end loss. The front-end circuit is a 0 Ω resistor.
Devices should operate in the center frequency range allocated by regional regulatory authorities. The target center frequency range and the target transmit power are configurable by software. See [ESP RF Test Tool](#) and [Test Guide](#) for instructions.

Unless otherwise stated, the RF tests are conducted with a 3.3 V (±5%) supply at 25 °C ambient temperature.

**Subtitle: Wi-Fi Radio (2.4 GHz)**

Table 6-1. Wi-Fi RF Characteristics

| Name | Description |
|------|-------------|
| Center frequency range of operating channel | 2412 ~ 2484 MHz |
| Wi-Fi wireless standard | IEEE 802.11b/g/n/ax |

**Subtitle: Wi-Fi RF Transmitter (TX) Characteristics**

Table 6-2. TX Power with Spectral Mask and EVM Meeting 802.11 Standards

| Rate | Min (dBm) | Type | Max (dBm) |
|------|-----------|------|-----------|
| 802.11b, 1 Mbps, DSSS | — | 21.0 | — |
| 802.11b, 11 Mbps, CCK | — | 21.0 | — |
| 802.11g, 6 Mbps, OFDM | — | 20.0 | — |
| 802.11g, 54 Mbps, OFDM | — | 19.0 | — |
| 802.11n, HT20, MCS0 | — | 19.0 | — |
| 802.11n, HT20, MCS7 | — | 18.0 | — |
| 802.11n, HT40, MCS0 | — | 18.5 | — |
| 802.11n, HT40, MCS7 | — | 17.5 | — |
| 802.11ax, HE20, MCS0 | — | 19.0 | — |
| 802.11ax, HE20, MCS9 | — | 15.0 | — |

Table 6-3. TX EVM Test

| Rate | Min (dB) | Type | Limit (dB) |
|------|----------|------|-----------|
| 802.11b, 1 Mbps, DSSS | — | -24.8 | -10.0 |
| 802.11b, 11 Mbps, CCK | — | -24.8 | -10.0 |

**Footer:**
Espressif Systems
Page number: 59

ESP32-C61 Series Datasheet v0.5