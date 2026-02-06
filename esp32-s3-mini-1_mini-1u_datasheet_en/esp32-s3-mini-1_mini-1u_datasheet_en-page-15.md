**Title: Boot Configurations**

In SPI Boot mode, the ROM bootloader loads and executes the program from SPI flash to boot the system.

In Joint Download Boot mode, users can download binary files into flash using UARTO or USB interface. It is also possible to download binary files into SRAM and execute it from SRAM.

In addition to SPI Boot and Joint Download Boot modes, ESP32-S3 also supports SPI Download Boot mode.
For details, please see [ESP32-S3 Technical Reference Manual > Chapter Chip Boot Control](#).

---

**4.2 VDD_SPI Voltage Control**

Depending on the value of EFUSE_VDD_SPIFORCE, the voltage can be controlled in two ways.

| Table 4-4: VDD_SPI Voltage Control |
|-------------------------------------|
| **VDD_SPI power source** | **Voltage** | **EFUSE_VDD_SPI FORCE** | **GPIO45** | **EFUSE_VDD_SPI_TIEH** |
| VDD3P3_RTC via RSP1 | 3.3 V | 0 | Ignored | Ignored |
| Flash Voltage Regulator | 1.8 V | - | 1 | - |
| Flash Voltage Regulator | 1.8 V | - | Ignore | 0 |
| VDD3P3_RTC via RSP1 | 3.3 V | 1 | - | 1 |

**Note:** Bold marks the default value and configuration.
See [ESP32-S3 Series Datasheet > Section Power Scheme](#).

---

**4.3 ROM Messages Printing Control**

During boot process, messages by the ROM code can be printed to:

- (Default) UARTO and USB Serial/JTAG controller
- USB Serial/JTAG controller

The ROM messages printing to UART or USB Serial/JTAG controller can be respectively disabled by configuring registers and eFuse.
For detailed information, please refer to [ESP32-S3 Technical Reference Manual > Chapter Chip Boot Control](#).

---

**4.4 JTAG Signal Source Control**

The strapping pin GPIO3 can be used to control the source of JTAG signals during early boot process.

This pin does not have any internal pull resistors and the strapping value must be controlled by external circuit that cannot in a high impedance state.
As Table 4-5 shows, GPIO3 is used in combination with EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_STRAP_JTAG_SEL.

---

**Footer:**

Espressif Systems
15

[Submit Documentation Feedback](#)