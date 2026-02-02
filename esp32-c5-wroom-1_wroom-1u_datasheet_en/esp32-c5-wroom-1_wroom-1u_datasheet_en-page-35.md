**Title: Electrical Characteristics**

---

**Note:**  
The content below is excerpted from Section Power Consumption in Other Modes in ESP32-C5 Series Datasheet.

---

### 6.4.2 Current Consumption in Other Modes

#### Table 6-8. Current Consumption in Modem-sleep Mode

| Mode       | CPU Frequency (MHz) | Description                | All Peripherals Typ (mA) | All Peripherals Clocks Disabled Typ (mA) | All Peripherals Clocks Enabled Typ (mA) |
|------------|----------------------|----------------------------|---------------------------|------------------------------------------|-----------------------------------------|
| WAITI      | 240                  | CPU while loop             | 18                        | 27                                       |                                          |
|            |                      | Run CoreMark               | 26                        | 35                                       |                                          |
|            |                      |                           | 34                        | 43                                       |                                          |
| WAITI      | 160                  | CPU while loop             | 20                        | 32                                       |                                          |
| Modem-sleep|                      | Run CoreMark               | 26                        | 37                                       |                                          |
|            |                      |                           | 15                        | 24                                       |                                          |
|            | 80                   | CPU while loop             | 15                        | 29                                       |                                          |
| WAITI      | 40                   | CPU while loop             | 8                         | 18                                       |                                          |
| Modem-sleep|                      | Run CoreMark               | 10                        | 19                                       |                                          |
|            |                      |                           | 12                        | 21                                       |                                          |

Footnotes:
1. In practice, the current consumption might be different depending on which peripherals are enabled.
2. In Modem-sleep mode, Wi-Fi is clock gated.
3. In Modem-sleep mode, the consumption might be higher when accessing flash.

---

#### Table 6-9. Current Consumption in Low-Power Modes

| Mode       | Description                | Typ (mA) |
|------------|----------------------------|----------|
| Light-sleep| CPU and wireless communication modules are powered down, peripheral clocks are disabled, and all GPIOs are high-impedance | 0.25     |
|            |                           |          | 0.06     |
| Deep-sleep | RTC timer and LP memory are powered on | 0.012    |
| Power off  | CHIP_PU is set to low level, the chip is powered off | 0.002   |

---

### 6.5 Memory Specifications

The data below is sourced from the memory vendor datasheet. These values are guaranteed through design and/or characterization but are not fully tested in production. Devices are shipped with the memory erased.

---

**Footer:**  
Espressif Systems  
35 ESP32-C5-WROOM-1 & WROOM-1U Datasheet v0.8  
Submit Documentation Feedback  
PRELIMINARY