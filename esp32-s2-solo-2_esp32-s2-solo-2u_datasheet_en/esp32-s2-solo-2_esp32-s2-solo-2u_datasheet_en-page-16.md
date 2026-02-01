**Title: Boot Configurations**

---

### Table-4-4, VDD_SPI Voltage Control

| VDD_SPI power source | Voltage | EFUSE_VDD_SPI FORCE | GPIO045 | EFUSE_VDD_SPI TIEH |
|-----------------------|---------|----------------------|----------|--------------------|
| VDD3P3_RTC via R_SPI  |         |                     | 3.3V     |                    | **0**    | **Ignore**   | **1**      | **Ignore** |
| Flash Voltage Regulator |        |                      | 1.8V     |                    |          |            |           |          |

1 Bold marks the default value and configuration.
2 See ESP32-S2 Series Datasheet > Section Power Scheme.

---

### Subtitle: ROM Messages Printing Control

During the boot process, the messages by the ROM code can be printed to:

- (Default) UART0
- UART1

EFUSE_UART_PRINT_CONTROL and GPIO46 control ROM messages printing to UART as shown in Table 4-5

#### UART ROM Message Printing Control.

EFUSE_UART_PRINT_CHANNEL controls if the ROM messages will be printed to UART0 or UART1.
- **0:** UART0
- **1:** UART1

---

### Table-4-5, UART ROM Message Printing Control

| UART ROM Code Printing | EFUSE_UART_PRINT_CONTROL | GPIO46 |
|------------------------|---------------------------|--------|
| Enabled                | 0                         | Ignored|
|                       | 1                         |         |
| Disabled               | 2                         |         |
|                       | 3                         |         |

1 Bold marks the default value and configuration.

---

### Subtitle: Chip Power-up and Reset

Once the power is supplied to the chip, its power rails need a short time to stabilize. After that, CHIP_PU – the pin used for power-up and reset – is pulled high to activate the chip. For information on CHIP_PU as well as power-up and reset timing, see Figure 4-2 and Table 4-6.

---

**Footer:**
Espressif Systems
16 ESP32-S2-SOLO-2 & SOLO-2U Datasheet v1.3

Submit Documentation Feedback