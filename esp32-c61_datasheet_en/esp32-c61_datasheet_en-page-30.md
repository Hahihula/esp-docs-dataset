**Title: Boot Configurations**

---

### Table 3-6. USB Serial/JTAG ROM Message Printing Control

| **USB Serial/JTAG ROM Message Printing Control** | LP_AON_STORE4_REG[0] | EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT |
| --- | --- | --- |
| Enabled | 0 | 0 |
| Disabled | 0 | 1 |

*Note: Bold marks the default value and configuration.*

---

### Section Title: 3.4 JTAG Signal Source Control

The strapping pin GPIO7 can be used to control the source of JTAG signals during the early boot process. This pin does not have any internal pull resistors and the strapping value must be controlled by the external circuit that cannot be in a high impedance state.

As Table 3-7 shows, GPIO7 is used in combination with EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_JTAG_SEL_ENABLE.

---

### Table 3-7. JTAG Signal Source Control

| eFuse1 | eFuse2 | eFuse3 | GPIO7 | JTAG Signal Source |
| --- | --- | --- | --- | --- |
| 0       | O      | x       | USB Serial/JTAG Controller |
|         |        |         |       |                      |
| 0       | X      | x       | JTAG pins MTDI, MTCK, MTMS and MTDO |
|         |        |         |       |                      |
| 1       | O      | x       | USB Serial/JTAG Controller |
|         |        |         |       |                      |
| 1       | X      | x       | JTAG is disabled |

*Note:*
- eFuse1, EFUSE_DIS_PAD_JTAG
- eFuse2, EFUSE_DIS_USB_JTAG
- eFuse3, EFUSE_JTAG_SEL_ENABLE

*x*: Indicates that the value has no effect on the result and can be ignored.

*Bold marks the default value and configuration.*

---

**Footer:**
Espressif Systems  
Page 30 ESP32-C61 Series Datasheet v0.5