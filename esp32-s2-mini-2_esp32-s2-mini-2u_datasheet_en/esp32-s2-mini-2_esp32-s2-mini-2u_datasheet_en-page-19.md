**Title: Electrical Characteristics**

---

### Table 5-5. Current Consumption in Modem-sleep Mode

| Mode          | CPU Frequency (MHz) | Description                           | All Peripherals Clocks Disabled (mA) | Typ |
|---------------|----------------------|---------------------------------------|----------------------------------------|-----|
|               |                      |                                       |                                        |     |
| Modem-sleep^2,3| 240                 | CPU is idle                           | 20.0                                   | 28.0|
|               |                      |                                       |                                        |     |
| Modem-sleep^2,3| 160                 | CPU is running                         | 14.0                                   | 21.0|
|               |                      |                                       |                                        |     |
| Modem-sleep^2,3| 80                  | CPU is idle                           | 10.5                                   | 18.4|
|               |                      |                                       |                                        |     |
| Modem-sleep^2,3| 80                  | CPU is running                         | 12.0                                   | 20.0|

**Footnotes:**
1 In practice, the current consumption might be different depending on which peripherals are enabled.
2 In Modem-sleep mode, Wi-Fi is clock gated.
3 In Modem-sleep mode, the consumption might be higher when accessing flash. For a flash rated at 80 Mbit/s, in SPI 2-line mode the consumption is 10 mA.

---

### Table 5-6. Current Consumption in Low-Power Modes

| Work mode    | Description                                                                                   | Typ (µA) |
|---------------|---------------------------------------------------------------------------------------------|----------|
| Light-sleep^1| VDD_SPI and Wi-Fi are powered down, and all GPIOs are high-impedance                        | 750      |
|               | The ULP co-processor is powered on^2                                                         |          |
| Deep-sleep    | ULP sensor-monitored pattern^3 RTC timer + RTC memory                                        | 190      |
|               | RTC timer only                                                                               | 22       |
| Power off     | CHIP_PU is set to low level, the chip is powered off                                         | 25       |

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

Espressif Systems

ESP32-S2-MINI-2 & MINI-2U Datasheet v1.3
Submit Documentation Feedback