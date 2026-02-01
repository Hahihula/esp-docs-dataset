**Title: Boot Configurations**

---

### Table 3-6. USB Serial/JTAG ROM Message Printing Control

| USB Serial/JTAG ROM Code Printing | EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT |
|------------------------------------|---------------------------------------|
| Enabled                            | O                                     |
| Disabled                           | 1                                     |

**Note:** Bold marks the default value and configuration.

---

### Section: 3.4 JTAG Signal Source Control

The strapping pin GPIO34 can be used to control the source of JTAG signals during the early boot process. This pin does not have any internal pull resistors, and the strapping value must be controlled by the external circuit that cannot be in a high impedance state.

As Table 3-7 JTAG Signal Source Control shows, GPIO34 is used in combination with EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_JTAG_SEL_ENABLE.

---

### Table 3-7. JTAG Signal Source Control

| JTAC Signal Source | EFUSE_DIS_PAD_JTAG | EFUSE_DIS_USB_JTAG | EFUSE_JTAG_SEL_ENABLE | GPIO34 |
|--------------------|---------------------|--------------------|------------------------|--------|
| USB Serial/JTAG Controller | O                   | 0                  | 1                      | Ignored |
| JTAC pins^2       | 1                   | 0                  | 1                      | Ignored |
| JTAC is disabled  | 0                   | 1                  | 1                      | Ignored |

**Note:** Bold marks the default value and configuration.

^2 JTAG pins refer to MTDI, MTCK, MTMS, and MTDO. 

---

**Footer:**
Espressif Systems
ESP32-P4 Series Datasheet v0.6

Submit Documentation Feedback