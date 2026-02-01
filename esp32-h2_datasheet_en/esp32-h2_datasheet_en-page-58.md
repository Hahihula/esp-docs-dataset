**Title:**
6 RF Characteristics

**Body Text:**
This section contains tables with RF characteristics of the Espressif product.

The RF data is measured at the antenna port, where RF cable is connected, including the front-end loss. The front-end circuit is a 0 Ω resistor.
Devices should operate in the center frequency range allocated by regional regulatory authorities. The target center frequency range and the target transmit power are configurable by software. See ESP RF Test Tool and [Test Guide](#) for instructions.

Unless otherwise stated, the RF tests are conducted with a 3.3 V (±5%) supply at 25 °C ambient temperature.

**Subtitle:**
6.1 Bluetooth LE Radio

**Table Title: Table 6-1. Bluetooth LE RF Characteristics**

| Name | Description |
|------|-------------|
| Center frequency range of operating channel | 2402 ~ 2480 MHz |
| RF transmit power range | -24.0 ~ 20.0 dBm |

**Subtitle:**
6.1.1 Bluetooth LE RF Transmitter (TX) Characteristics

**Table Title: Table 6-2. Bluetooth LE - Transmitter Characteristics - 1 Mbps**

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| Carrier frequency offset and drift | Max. \( \left\lceil f_n \right\rceil_{n=0, 1, 2, 3, ...k} \) | — | 1.5 | — | kHz |
| | Max. \( \left\lceil f_0 - f_n \right\rceil_{n=2, 3, 4, ...} \) | — | 2.8 | — | kHz |
| | Max. \( \left\lceil f_n - f_{n-5} \right\rceil_{n=6, 7, 8, ...k} \) | — | 1.3 | — | kHz |
| | \( \left\lceil f_1 - f_0 \right\rceil \) | — | 2.3 | — | kHz |
| Modulation characteristics | Δ\( F_{avg} \) | 251.8 | kHz | — | kHz |
| | Min. \( \Delta F_{2max} \) (for at least 99.9% of all \( \Delta F_{2max} \)) | - | 217.0 | — | kHz |
| | Δ\( F_{avg}/F_1 \) | – | 0.87 | — | — |
| In-band emissions | ± 2 MHz offset | – | −28 | dBm | — |
| | ± 3 MHz offset | - | −32 | dBm | — |
| | > ± 3 MHz offset | - | −34 | dBm | — |

**Table Title: Table 6-3. Bluetooth LE - Transmitter Characteristics - 2 Mbps**

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| Carrier frequency offset and drift | Max. \( \left\lceil f_n \right\rceil_{n=0, 1, 2, 3, ...k} \) | — | 3.3 | kHz | — |
| | Max. \( \left\lceil f_0 - f_n \right\rceil_{n=2, 3, 4, ...} \) | — | 3.3 | kHz | — |
| | Max. \( \left\lceil f_n - f_{n-5} \right\rceil_{n=6, 7, 8, ...k} \) | — | 1.6 | kHz | — |
| | \( \left\lceil f_1 - f_0 \right\rceil \) | — | 2.3 | kHz | — |

**Footer:**
Espressif Systems
ESP32-H2 Series Datasheet v1.2

**Note:** Cont’d on next page