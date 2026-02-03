**Chapter Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Table Header:**
Table 33.5- JTAG Capabilities Descriptor

| Byte | Value | Description |
|------|-------|-------------|
| O    | 1     | JTAG protocol capabilities structure version |
| 1    | 10    | Total length of JTAG protocol capabilities |
| 2    | 1     | Type of this struct: 1 for speed capabilities struct |
| 3    | 8     | Length of this speed capabilities struct |
| 4 ~ 5 | 8000  | APB_CLK speed in 10 kHz increments. Note that the maximal TCK speed is half of this |
| 6 ~ 7 | 1     | Minimum divisor settable by the VEND_JTAG_SETDIV request |
| 8 ~ 9 | 255   | Maximum divisor settable by the VEND_JTAG_SETDIV request |

**Section Title:**
33.4 Recommended Operation

**Subsection Title and Content:**
33.4.1 Internal/external PHY Selection
- As the ESP32-S3 only has a single internal PHY, at first programming you may need to decide how that is going to be used in the intended application by burning eFuses to affect the initial USB configuration. This affects ROM download mode as well: while both USB-OTG and also the USB Serial/JTAG controller allows serial programming, only USB-OTG supports the DFU protocol and only the USB Serial/JTAG controller supports JTAG debugging over USB. Even when not using USB, eFuse configuration is required when an external JTAG adapter will be used.

**Table Title:**
Table 33.4-1 Use cases and eFuse settings

| Use case | eFuses | Note |
|----------|--------|------|
| USB serial/JTAG on internal PHY only | None | - |
| USB OTG on internal PHY only | EFUSE_USB_PHY_SEL + JTAG on GPIO pins | - |
| USB serial/JTAG on external PHY, OTG on external PHY | EFUSE_DIS_USB_JTAG | - |
| USB OTG on internal PHY, USB serial/JTAG on external | EFUSE_USB_PHY_SEL | - |

**Additional Information:**
After the user program is running, it can modify the initial configuration by setting registers. Specifically,
- RTC_CNTL_SW_HW_USB_PHY_SEL can be used to have software override the effect of
- EFUSE_USB_PHY SEL: if this bit is set, the USB PHY selection logic will use the value of the
- RTC_CNTL_SW_USB_PHY_SEL in place of that of EFUSE_USB_PHY_SEL.

As shown in 33.3-1, by default (phy_sel = 0), ESP32-S3 USB Serial/JTAG Controller is connected to internal PHY and USB-OTG is connected to external PHY. However, when USB-OTG Download mode is enabled, the chip initializes the IO pad connected to the external PHY in ROM when starts up. The status of each IO pad after initialization is as follows.

**Footer:**
Espressif Systems  
1252  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback]