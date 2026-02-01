**Title: RF Characteristics**

This section contains tables with RF characteristics of the Espressif product.

The RF data is measured at the antenna port, where RF cable is connected, including the front-end loss. The external antennas used for the tests on the modules with external antenna connectors have an impedance of 50 Ω.
Devices should operate in the center frequency range allocated by regional regulatory authorities. The target center frequency range and the target transmit power are configurable by software.

**Link:** [ESP RF Test Tool](#) and **Link:** [Test Guide](#)

Unless otherwise stated, the RF tests are conducted with a 3.3 V (±5%) supply at 25 °C ambient temperature.

---

**Subtitle: Wi-Fi Radio**

6.1

**Sub-subtitle: Wi-Fi RF Standards**

6.1.1

**Table Title:** Table 6-1. Wi-Fi RF Standards

| Name | Description |
|------|-------------|
| Center frequency range of operating channel^1 | 2412 ~ 2484 MHz |
| Wi-Fi wireless standard | IEEE 802.11b/g/n |
| Data rate | - 20 MHz: 802.11b: 1, 2, 5.5 and 11 Mbps<br>- 802.11g: 6, 9, 12, 18, 24, 36, 48, 54 Mbps<br>- 802.11n: MCS0-7, 72.2 Mbps (Max) |
| Antenna type | PCB antenna, external antenna connector |

^1 Device should operate in the center frequency range allocated by regional regulatory authorities.
Target center frequency range is configurable by software.

**Footnote:** See **Link:** [ESP RF Test Tool and Test Guide](#)

For the modules that use external antenna connectors, the output impedance is 50 Ω. For other modules without external antenna connectors, the output impedance is irrelevant.

---

**Subtitle: Wi-Fi RF Transmitter (TX) Specifications**

6.1.2

Target TX power is configurable based on device or certification requirements. The default characteristics are provided in Table 6-2.

**Table Title:** Table 6-2. TX Power with Spectral Mask and EVM Meeting 802.11 Standards

| Rate | Min (dBm) | Type (dBm) | Max (dBm) |
|------|-----------|------------|-----------|
| 802.11b, 1 Mbps | — | 19.5 | — |
| 802.11b, 11 Mbps | — | 19.5 | — |
| 802.11g, 6 Mbps | — | 17.5 | — |

**Continuation:** Cont'd on next page

---

Espressif Systems  
Page: 22  
Document Title: ESP32-S2-SOLO-2 & SOLO-2U Datasheet v1.3  

**Links and References**: 
- [ESP RF Test Tool](#)
- [Test Guide](#)