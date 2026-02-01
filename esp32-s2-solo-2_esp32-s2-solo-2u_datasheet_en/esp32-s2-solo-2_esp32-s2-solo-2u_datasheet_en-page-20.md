**Title: Electrical Characteristics**

---

### Table 5-5. Current Consumption in Modem-sleep Mode

| Mode          | CPU Frequency (MHz) | Description                          | All Peripherals Clocks Disabled (mA) | Typ |
|---------------|----------------------|--------------------------------------|---------------------------------------|-----|
|               |                      |                                      | All Peripherals Clocks Enabled (mA)  |     |
| Modem-sleep^2,3| -                   | CPU is idle                          |                                       | 1   |
|                | 240                  |                                      |                                        | 20.0|
|                |                      | CPU is running                        |                                        | 28.0|
|                | 160                  | CPU is idle                          |                                        | 14.0|
|                |                      | CPU is running                        |                                        | 21.0|
|                | -                    |                                      |                                        | 16.0|
|                | 80                   | CPU is idle                          |                                        | 10.5|
|                |                      | CPU is running                        |                                        | 18.4|
|                | -                    |                                      |                                        | 12.0|
|                | -                    |                                      |                                        | 20.0|

**Footnotes:**
1 In practice, the current consumption might be different depending on which peripherals are enabled.
2 In Modem-sleep mode, Wi-Fi is clock gated.
3 In Modem-sleep mode, the consumption might be higher when accessing flash. For a flash rated at 80 Mbit/s, in SPI 2-line mode the consumption is 10 mA.

---

### Table 5-6. Current Consumption in Low-Power Modes

| Work mode    | Description                                    | Typ (µA) |
|---------------|-------------------------------------------------|----------|
| Light-sleep^1| VDD_SPI and Wi-Fi are powered down, and all GPIOs are high-impedance | 750      |
|               | The ULP co-processor is powered on              |         |
| Deep-sleep    | ULP sensor-monitored pattern                    | 22       |
|               | RTC timer + RTC memory                          |         |
|               | RTC timer only                                   |         |
| Power off     | CHIP PU is set to low level, the chip is powered off | 1        |

**Footnotes:**
1 In Light-sleep mode, with all related SPI pins pulled up, the current consumption of the embedded PSRAM is 140 µA. Chip variants with in-package PSRAM include ESP32-S2FN4R2 and ESP32-S2R2.
2 During Deep-sleep, when the ULP co-processor is powered on, peripherals such as GPIO and I2C are able to operate.

---

### 5.5 Memory Specifications

The data below is sourced from the memory vendor datasheet. These values are guaranteed through design and/or characterization but are not fully tested in production. Devices are shipped with the memory erased.

**Table 5-7. Flash Specifications**

| Parameter | Description                   | Min   | Typ    | Max   | Unit |
|-----------|-------------------------------|-------|--------|-------|------|
| VCC       | Power supply voltage (1.8 V) | 1.65  | 1.80   | 2.00  | V    |

**Continued on next page**

---

*Espressif Systems*
*Submit Documentation Feedback*

Page: **20**
Datasheet version: **v1.3**