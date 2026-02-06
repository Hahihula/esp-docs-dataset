**Title: Electrical Characteristics**

---

### Table 6-6. Current Consumption in Modem-sleep Mode

| Work mode | Frequency (MHz) | Description                                                                                   | Typ1 (mA) | Typ2 (mA) |
|-----------|------------------|------------------------------------------------------------------------------------------------|------------|-----------|
|           |                  | WAITI (Dual core in idle state)                                                                | 13.2       | 18.8      |
|           | **40**           | Single core running 32-bit data access instructions, the other core in idle state                | 16.2       | 21.8      |
|           |                  | Dual core running 32-bit data access instructions                                              | 18.7       | 24.4      |
|           | **80**           | Single core running 128-bit data access instructions, the other core in idle state               | 19.9       | 25.4      |
|           |                  | Dual core running 128-bit data access instructions                                              | 23.0       | 28.8      |
|           | **Modem-sleep³** | WAITI                                                                                           | 22.0       | 36.1      |
|           | **160**          | Single core running 32-bit data access instructions, the other core in idle state               | 27.6       | 42.3      |
|           |                  | Dual core running 128-bit data access instructions                                              | 39.9       | 54.6      |
|           | **240**          | Single core running 128-bit data access instructions, the other core in idle state               | 49.6       | 64.1      |
|           |                  | Dual core running 32-bit data access instructions                                              | 54.4       | 69.2      |
|           | **Modem-sleep³** | WAITI                                                                                           | 66.7       | 81.1      |
|           | **320**          | Single core running 32-bit data access instructions, the other core in idle state               | 54.9       | 69.2      |
|           |                  | Dual core running 128-bit data access instructions                                              | 72.4       | 87.9      |
|           | **320**          | Single core running 128-bit data access instructions, the other core in idle state               | 91.7       | 107.9     |

Footnotes:
1. Current consumption when all peripheral clocks are disabled.
2. Current consumption when all peripheral clocks are enabled. In practice, the current consumption might be different depending on which peripherals are enabled.
3. In Modem-sleep mode, Wi-Fi is clock gated, and the current consumption might be higher when accessing flash. For a flash rated at 80 Mbit/s, in SPI 2-line mode the consumption is ~10 mA.

---

### Table 6-7. Current Consumption in Low-Power Modes

| Work mode | Description                                                                                   | Typ (µA) |
|-----------|----------------------------------------------------------------------------------------------|----------|
| Light-sleep¹ | VDD_SPI and Wi-Fi are powered down, and all GPIOs are high-impedance.                       | **240**  |
| Deep-sleep | RTC memory and RTC peripherals are powered up. RTC peripheral is powered down.               |          | **8**     |
|             | RTC memory is power up. RTC peripherals are powered down.                                   |          | **7**     |

Footnotes:
1. In Low-power mode, VDD_SPI clock gate can be disabled.

---

*Espressif Systems*
*31*  
*ESP32-S3-MINI-1 & MINI-1U Datasheet v1.6*

[Submit Documentation Feedback](#)