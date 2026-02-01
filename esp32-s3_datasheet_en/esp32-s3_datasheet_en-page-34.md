**Title: Boot Configurations**

For details, please see [ESP32-S3 Technical Reference Manual > Chapter Chip Boot Control](#).

---

### Section Title

#### Subsection 3.2 VDD_SPI Voltage Control

The required VDD_SPI voltage for the chips of the ESP32-S3 Series can be found in Table **1-1 ESP32-S3 Series Comparison**.

The VDD_SPI voltage can be:
- (Default) 3.3 V supplied by VDDSP3_RTC via R\_{SPI}
- 1.8V supplied by the Flash Voltage Regulator

The voltage is determined by EFUSE_VDD_SPI FORCE, GPIO45, and EFUSE_VDD_SPI_TIEH.

**Table Title: Table 3-4. VDD_SPI Voltage Control**

| VDD_SPI power source | Voltage | EFUSE_VDD_SPI FORCE | GPIO45 | EFUSE_VDD_SPI TIEH |
|-----------------------|---------|----------------------|--------|--------------------|
| VDDSP3_RTC via R\_{SPI} | 3.3 V   | 0                    | 0      | Ignored            |
| Flash Voltage Regulator |         | 1                    | 1      | Ignored            |

**Note:** Bold marks the default value and configuration.

---

#### Subsection 3.3 ROM Messages Printing Control

During the boot process, the messages by the ROM code can be printed to:
- (Default) UARTO and USB Serial/JTAG controller
- USB Serial/JTAG controller
- UARTO

The ROM messages printing to UART or USB Serial/JTAG controller can be respectively disabled by configuring registers and eFuse. For detailed information, please refer to [ESP32-S3 Technical Reference Manual > Chapter Chip Boot Control](#).

---

#### Subsection 3.4 JTAG Signal Source Control

The strapping pin GPIO3 can be used to control the source of JTAG signals during the early boot process. This pin does not have any internal pull resistors and the strapping value must be controlled by the external circuit that cannot be in a high impedance state.

As Table **3-5 JTAG Signal Source Control** shows, GPIO3 is used in combination with EFUSE\_DIS\_PAD\_JTAG, EFUSE\_DIS\_USB\_JTAG, and EFUSE\_STRAP\_JTAG\_SEL. 

---

*Footer:*
Espressif Systems  
Page 34 of ESP32-S3 Series Datasheet v2.1

[Submit Documentation Feedback](#)