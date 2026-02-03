**Title: Electrical Characteristics**

---

**Note:**  
The content below is excerpted from Section Current Consumption in Other Modes in ESP32-C61 Series Datasheet.

---

### 6.4.2 Current Consumption in Other Modes

#### Table 17: Current Consumption in Modem-sleep Mode

| Mode          | CPU Frequency (MHz) | Description                          | All Peripherals Typ (mA) | All Peripherals Clocks Disabled/Enabled |
|---------------|----------------------|--------------------------------------|--------------------------|-----------------------------------------|
| WAITI         |                      |                                      |                         |                                          |
| Modem-sleep2,3 | 160                  | CPU while loop                       | 16                       | 23                                       |
|               |                      | Run CoreMark                          | 21                       | 28                                       |
|               |                      | WAITI                                 | 10                       | 16                                       |
| Modem-sleep   | 80                   | CPU while loop                       | 12                       | 19                                       |
|               |                      | Run CoreMark                          | 15                       | 21                                       |
|               |                      | WAITI                                 | 6                        | 11                                       |
| Modem-sleep   | 40                   | CPU while loop                       | 7                        | 12                                       |
|               |                      | Run CoreMark                          | 9                        | 13                                       |

**Footnotes:**
1. In practice, the current consumption might be different depending on which peripherals are enabled.
2. In Modem-sleep mode, Wi-Fi is clock gated.
3. In Modem sleep mode, the consumption might be higher when accessing flash.

---

#### Table 18: Current Consumption in Low-Power Modes

| Mode          | Description                          | Typ (mA) |
|---------------|--------------------------------------|----------|
| Light-sleep   | CPU and wireless communication modules are powered down, peripheral clocks are disabled, and all GPIOs are high-impedance. | 0.2      |
|               |                                      | CPU, with wireless communication modules and peripherals are powered down, and all GPIOs are high-impedance. | 0.05     |
| Deep-sleep    | LP timer and LP memory are powered on | 0.01     |
| Power off     | CHIP_PU is set to low level, the chip is powered off | 0.001   |

---

**Footer:**  
Espressif Systems  
27 ESP32-C61-MINI-1 & MINI-1U Datasheet v0.6  

[Submit Documentation Feedback](#)