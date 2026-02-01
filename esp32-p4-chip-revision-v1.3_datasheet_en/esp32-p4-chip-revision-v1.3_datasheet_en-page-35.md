**Title: Boot Configurations**

In Joint Download Boot mode, users can download binary files into flash using USB, UARTO, or SPI slave interface. It is also possible to download binary files into L2MEM and execute them from L2MEM.

In addition to SPI Boot and Joint Download Boot modes, ESP32-P4 also supports SPI Download Boot mode.
For details, please see [ESP32-P4 Technical Reference Manual > Chapter Chip Boot Control](#).

---

**Subtitle: 3.2 VDDO_FLASH Voltage Control**

ESP32-P4 supplies power to flash via VDDO_FLASH, which outputs 3.3 V by default. After burning EFUSE_OPXA_TIEH_SEL_0, the output changes to 1.8 V.

**Table Title:** Table 3-4. VDDO_FLASH Voltage Control

| VDDO_FLASH power source | EFUSE_OPXA_TIEH_SEL_0 | Voltage |
|--------------------------|------------------------|---------|
| Flash LDO               | 0                      | 3.3 V   |
|                          | 1                      | 1.8 V   |

**Notes:**
- Bold marks the default value and configuration.
- See Section [2.6.2 Power Scheme](#).

---

**Subtitle: 3.3 ROM Messages Printing Control**

During the boot process, the messages by the ROM code can be printed to:
- (Default) UARTO and USB Serial/JTAG controller
- USB Serial/JTAG controller

EFUSE_UART_PRINT_CONTROL and GPIO36 control ROM messages printing to UARTO as shown in Table 3-5.

**Table Title:** Table 3-5. UARTO ROM Message Printing Control

| UARTO ROM Code Printing | EFUSE_UART_PRINT_CONTROL | GPIO36 |
|-------------------------|----------------------------|--------|
| Enabled                 | 0                          | Ignored|
|                         | 1                          | 0      |
|                         | 2                          | 1      |
| Disabled                | 1                          | 1      |
|                         | 2                          | 0      |
|                         | 3                          | Ignored|

**Notes:**
- Bold marks the default value and configuration.

EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT controls the printing to USB Serial/JTAG controller as shown in Table [3-6 USB Serial/JTAG ROM Message Printing Control](#).

---

**Footer:**  
Espressif Systems  
Page 35 of ESP32-P4 Series Datasheet v0.6

[Submit Documentation Feedback](#)