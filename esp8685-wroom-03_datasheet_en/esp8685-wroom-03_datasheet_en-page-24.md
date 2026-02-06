**Title: RF Characteristics**

This section contains tables with RF characteristics of the Espressif product.

The RF data is measured at the antenna port, where RF cable is connected, including the front-end loss. Devices should operate in the center frequency range allocated by regional regulatory authorities. The target center frequency range and the target transmit power are configurable by software. See [ESP RF Test Tool](#) and [Test Guide](#) for instructions.

Unless otherwise stated, the RF tests are conducted with a 3.3 V (±5%) supply at 25 °C ambient temperature.

---

**Subtitle: Wi-Fi Radio**

**Table Title: Table 7-1, Wi-Fi RF Characteristics**

| Name | Description |
|------|-------------|
| Center frequency range of operating channel | 2412 ~ 2484 MHz |
| Wi-Fi wireless standard | IEEE 802.11b/g/n |

---

**Subtitle: Wi-Fi RF Transmitter (TX) Characteristics**

**Table Title: Table 7-2, TX Power with Spectral Mask and EVM Meeting 802.11 Standards**

| Rate | Min (dBm) | Type | Max (dBm) |
|------|-----------|------|-----------|
| 802.11b, 1 Mbps | — | 20.0 | — |
| 802.11b, 11 Mbps | — | 20.0 | — |
| 802.11g, 6 Mbps | — | 19.5 | — |
| 802.11g, 54 Mbps | — | 17.5 | — |
| 802.11n, HT20, MCS0 | — | 18.5 | — |
| 802.11n, HT20, MCS7 | — | 17.0 | — |
| 802.11n, HT40, MCS0 | — | 18.0 | — |
| 802.11n, HT40, MCS7 | — | 16.5 | — |

**Table Title: Table 7-3, TX EVM Test**

| Rate | Min (dB) | Type SL | Max (dB) |
|------|----------|---------|----------|
| 802.11b, 1 Mbps, @20 dBm | — | -24.5 | -10 |
| 802.11b, 11 Mbps, @20 dBm | — | -25.0 | -10 |
| 802.11g, 6 Mbps, @19.5 dBm | — | -24.5 | -5 |
| 802.11g, 54 Mbps, @17.5 dBm | — | -29.5 | -25 |
| 802.11n, HT20, MCS0, @18.5 dBm | — | -25.5 | -5 |

---

**Footer:**

Espressif Systems  
[Submit Documentation Feedback](#) ESP8685-WROOM-03 Datasheet v1.5

Page 24