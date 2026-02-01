**Title: Boot Configurations**

---

### Table Title:
Table 3-7. JTAG Signal Source Control

| **JTAG Signal Source** | eFuse1^2 | eFuse2^3 | eFuse3^4 | GPIO7 |
|------------------------|-----------|----------|----------|-------|
| USB Serial/JTAG Controller | O | X | - | 0 |
| JTAG pins MTDI, MTCK, MTMS, and MTDO | x | o | - | 1 |
| USB Serial/JTAG Controller^6 | 1 | o | x | x |
| **JTAG is disabled** | 1 | x | - | |

### Footnotes:
1. Bold marks the default value and configuration.
2. eFuse: EFUSE_DIS_PAD_JTAG
3. eFuse: EFUSE_DIS_USB_JTAG
4. eFuse: EFUSE_SEL_ENABLE
5. X: indicates that the value has no effect on the result and can be ignored.

### Additional Information:
- In Joint Download Boot 1 mode, the USB Serial/JTAG controller is forcibly disabled, and the JTAG signal only comes from JTAG pins.
- If PAD_JTAG is also disabled, then JTAG is disabled. 

---

**Footer:**
Espressif Systems  
ESP32-C5 Series Datasheet v1.0

[Submit Documentation Feedback](#)