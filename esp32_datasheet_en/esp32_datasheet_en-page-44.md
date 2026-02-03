**Title: Functional Description**

- Half-duplex (CSMA/CD) and full-duplex operation
- MAC control sublayer (control frames)
- 32-bit CRC generation and removal
- Several address-filtering modes for physical and multicast address (multicast and group addresses)
- 32-bit status code for each transmitted or received frame
- Internal FIFOs to buffer transmit and receive frames. The transmit FIFO and the receive FIFO are both 512 words (32-bit)
- Hardware PTP (Precision Time Protocol) in accordance with IEEE 1588 2008 (PTP V2)
- 25 MHz/50 MHz clock output

For details, see [ESP32 Technical Reference Manual](#) > Chapter Ethernet Media Access Controller (MAC).

---

**Title: Pin Assignment**

For information about the pin assignment of Ethernet MAC Interface, see Section **4.10 Peripheral Pin Configurations and ESP32 Technical Reference Manual** > Chapter IO_MUX and GPIO Matrix.

---

**Title: Analog Peripherals**

**Subtitle: 4.9 Analog-to-Digital Converter (ADC)**

ESP32 integrates two 12-bit SAR ADCs and supports measurements on 18 channels (analog-enabled pins). The ULP coprocessor in ESP32 is also designed to measure voltage, while operating in the sleep mode, which enables low-power consumption. The CPU can be woken up by a threshold setting and/or via other triggers.

**Table: ADC Characteristics**

| Parameter       | Description                                                                                   | Min  | Max   | Unit |
|-----------------|----------------------------------------------------------------------------------------------|------|-------|------|
| RTC controller; ADC connected to an DNL (Differential nonlinearity) external 100 nF capacitor; DC signal input; ambient temperature at 25 °C; INL (Integral nonlinearity) Wi-Fi&Bluetooth off | -7   | 7     | LSB  |
| Sampling rate    | RTC controller                                                                               | —    | 200   | kspS |
| DIG controller   |                                                                                              | —    | 2     | Msps |

**Notes:**
- When atten = 3 and the measurement result is above 3000 (voltage at approx. 2450 mV), the ADC accuracy will be worse than described in the table above.
- To get better DNL results, users can take multiple sampling tests with a filter, or calculate the average value.

---

**Footer:**
Espressif Systems
ESP32 Series Datasheet v5.2

[Submit Documentation Feedback](#)