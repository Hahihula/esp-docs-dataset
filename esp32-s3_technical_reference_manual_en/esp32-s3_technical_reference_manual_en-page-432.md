**Title: Chapter 5 eFuse Controller**

**Subtitle: Register 5.13. EFUSE_RD_REPEAT_DATAO_REG (0x0030)**

---

Continued from the previous page...

**Body Text and Descriptions:**
- **EFUSE_USB_EXCHG_PINS**: Represents whether or not USB D+ and D- pins are swapped.
  - Value `1`: Swapped. 
  - Value `0`: Not swapped.

- Note:
  The eFuse has a design flaw and does *not* move the pullup (needed to detect USB speed), resulting in the PC thinking the chip is a low-speed device, which stops communication. For detailed information, please refer to Chapter **33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)**.

- **EFUSE_EXT_PHY_ENABLE**: Represents whether the external PHY is enabled or disabled.
  - Value `0`: Disabled. 
  - Value `1`: Enabled.

---

**Footer:**
Espressif Systems
432 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback