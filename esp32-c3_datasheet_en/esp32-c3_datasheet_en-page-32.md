**Title: Boot Configurations**

- **UARTO**
- USB Serial/JTAG controller

EFUSE_UART_PRINT_CONTROL and GPIO8 control ROM messages printing to UARTO as shown in Table 3-4.

**Subtitle: UARTO ROM Message Printing Control**

**Table Title:** Table 3-4. UARTO ROM Message Printing Control

| UARTO ROM Code Printing | EFUSE_UART_PRINTControl | GPIO8 |
|-------------------------|--------------------------|-------|
| Enabled                 | 0                         | Ignored |
|                        | 1                         | 0      |
| Disabled                | 2                         | 1      |
|                        | 3                         | Ignored |

**Note:** Bold marks the default value and configuration.

EFUSE_USB_PRINT_CHANNEL controls the printing to USB Serial/JTAG controller as shown in Table 3-5 USB Serial/JTAG ROM Message Printing Control.

**Table Title:** Table 3-5. USB Serial/JTAG ROM Message Printing Control

| USB Serial/JTAG | EFUSE_DIS_USB_SERIAL_JTAG^2 | EFUSE_USB_PRINT_CHANNEL |
|------------------|-------------------------------|-------------------------|
| ROM Code Printing|                               |                        |
| Enabled          | O                             | o                       |
| Disabled         | 0                             | 1                       |

**Note:** Bold marks the default value and configuration.

EFUSE_DIS_USB_SERIAL_JTAG controls whether to disable USB Serial/JTAG. 

---

Espressif Systems  
32  
ESP32-C3 Series Datasheet v2.2  

[Submit Documentation Feedback](#)