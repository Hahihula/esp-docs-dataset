**Title:**
5 Electrical Characteristics

**Table Title:**
Table 5-9. Current Consumption in Low-Power Modes

| Mode       | Description                                                                                   | Typ (mA) |
|------------|------------------------------------------------------------------------------------------------|----------|
| Light-sleep| CPU and wireless communication modules are powered down, peripheral clocks are disabled, and all GPIOs are high-impedance | 0.2      |
|            | CPU, wireless communication modules and peripherals are powered down, and all GPIOs are high-impedance |          | 0.05     |
| Deep-sleep | LP timer and LP memory are powered on                                                          | 0.01     |
| Power off  | CHIP_PU is set to low level, the chip is powered off                                          | 0.001    |

**Footer:**
Espressif Systems
Page number: 58
ESP32-C61 Series Datasheet v0.5

**Watermark Text:** PRELIMINARY