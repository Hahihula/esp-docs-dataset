**Title: Boot Configurations**

---

### Table 4-4. VDD_SPI Voltage Control

| VDD_SPI power source | Voltage | EFUSE_VDD_SPI FORCE | GPIO045 | EFUSE_VDD_SPI TIEH |
|-----------------------|---------|----------------------|----------|--------------------|
| VDD3P3_RTC via R_SPI | 3.3 V   | 0                   | Ignore   | Ignored            |
| Flash Voltage Regulator |         | 1                   |          | 1                  |
|                        | 1.8 V   | 0                   | Ignore   | 0                  |

**Footnote:**
1 Bold marks the default value and configuration.
2 See ESP32-S2 Series Datasheet > Section Power Scheme.

---

### Subtitle: ROM Messages Printing Control

During the boot process, the messages by the ROM code can be printed to:

- (Default) UARTO
- UART1

EFUSE_UART_PRINT_CONTROL and GPIO46 control ROM messages printing to UART as shown in Table 4-5

**Table Title:** UART ROM Message Printing Control.

| UART ROM Code Printing | EFUSE_UART_PRINT_CONTROL | GPIO46 |
|------------------------|---------------------------|--------|
| Enabled                | 0                         | Ignored|
| Disabled               | 1                         |         |

**Footnote:**
1 Bold marks the default value and configuration.
2

---

### Subtitle: Chip Power-up and Reset

Once the power is supplied to the chip, its power rails need a short time to stabilize. After that, CHIP_PU – the pin used for power-up and reset – is pulled high to activate the chip. For information on CHIP_PU as well as power-up and reset timing, see Figure 4-2 and Table 4-6.

---

**Footer:**
Espressif Systems
15 ESP32-S2-MINI-2 & MINI-2U Datasheet v1.3

[Submit Documentation Feedback](#)