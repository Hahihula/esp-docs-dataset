**Title: Boot Configurations**

---

### **3.2 SDIO Sampling and Driving Clock Edge Control**

The strapping pin MTMS and MTDI can be used to decide on which clock edge to sample signals and drive output lines. See Table 3-4 [SDIC Input Sampling Edge/Output Driving Edge Control](#).

**Table:**
| Edge behavior | MTMS       | MTDI      |
|----------------|------------|-----------|
| Falling edge sampling, falling edge output | 0         | 0         |
| Falling edge sampling, rising edge output | 0         | 1         |
| Rising edge sampling, falling edge output | 1         | 0         |
| Rising edge sampling, rising edge output | 1         | 1         |

**Note:** MTMS and MTDI are floating by default. So above configurations.

---

### **3.3 ROM Messages Printing Control**

During the boot process, ROM message printing is enabled if LP_AON_STORE4_REG[0] is O (default), and disabled if LP_AON_STORE4_REG[0] is 1. When ROM message printing is enabled, the messages can be printed to:

- (Default) UARTO and USB Serial/JTAG controller
- USB Serial/JTAG controller
- UARTO

EFUSE_UART_PRINT_CONTROL and GPIO8 control ROM messages printing to UARTO as shown in Table 3-5 [UARTO ROM Message Printing Control](#).

**Table:**
| UARTO ROM Code Printing | EFUSE_UART_PRINT_CONTROL | GPIO8 |
|-------------------------|---------------------------|-------|
|                         | O                        | Ignored |
| Enabled                 | 1                        | 0      |
| Disabled                | 2                        | 1      |
|                         | 1                        | 1      |
|                         | 2                        | 0      |
|                         | 3                        | Ignored |

**Note:** Bold marks the default value and configuration.

---

EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT controls the printing to USB Serial/JTAG controller as shown in Table 3-6 [USB Serial/JTAG ROM Message Printing Control](#).

---

**Footer:**
Espressif Systems  
ESP32-C6 Series Datasheet v1.4

[Submit Documentation Feedback](#)