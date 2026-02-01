**Title: Boot Configurations**

---

### Table-34: VDD_SPI Voltage Control

| VDD_SPI power source | Voltage | EFUSE_VDD_SPI FORCE | GPIO45 | EFUSE_VDD_SPI TIEH |
|-----------------------|---------|----------------------|---------|--------------------|
| VDDP3P3_RTC via RSPI  |         |                     | 0       | Ignored            |
|                        | 3.3 V   |                      | 1       |                    |
| Flash Voltage Regulator |        |                      | 1.8 V   |                    |
|                        |         |                      | 1       | Ignored            |

**Note:** Bold marks the default value and configuration.

2 See Section [2.5.2 Power Scheme](#).

---

### Subtitle: ROM Messages Printing Control

During the boot process, messages by the ROM code can be printed to:

- (Default) UART0
- UART1

EFUSE_UART_PRINT_CONTROL and GPIO46 control ROM messages printing to UART as shown in Table 3-5.

**Table Title:** UART ROM Message Printing Control.
**Table Description:**
EFUSE_UART_PRINT_CHANNEL controls if the ROM messages will be printed to UART0 or UART1:

|           | 0       | 1        |
|-----------|---------|----------|
| UART0    | O       |          |
| UART1    |         |         |

---

### Table-35: UART ROM Message Printing Control

| UART ROM Code Printing | EFUSE_UART_PRINT CONTROL | GPIO46 |
|------------------------|---------------------------|--------|
| Enabled                | 0                         | Ignored|
| Disabled               | 2                         | 1      |
|                        | 3                         | 0      |

**Note:** Bold marks the default value and configuration.

---

**Footer:**
Espressif Systems
ESP32-S2 Series Datasheet v1.8

Submit Documentation Feedback