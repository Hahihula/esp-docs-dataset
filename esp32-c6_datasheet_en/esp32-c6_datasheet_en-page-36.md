**Title: Boot Configurations**

---

### Table 3-6. USB Serial/JTAG ROM Message Printing Control

| Description | EFUSE_DIS_USB_SERIAL_JTAG | EFUSE_DIS_USB_SERIAL_ROM_PRINT |
|-------------|---------------------------|--------------------------------|
| **USB Serial/JTAG ROM Code Printing** | - | - |
| Enabled     | `0`                       | `0`                             |
| Disabled    | `0`                       | `1`                             |

- Bold marks the default value and configuration.
- EFUSE_DIS_USB_SERIAL_JTAG controls whether to disable USB Serial/JTAG.

---

### 3.4 JTAG Signal Source Control

The strapping pin GPIO15 can be used to control the source of JTAG signals during the early boot process. This pin does not have any internal pull resistors and the strapping value must be controlled by the external circuit that cannot be in a high impedance state.

As Table 3-7 JTAG Signal Source Control shows, GPIO15 is used in combination with EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG and EFUSE_JTAG_SEL_ENABLE.

---

### Table 3-7. JTAG Signal Source Control

| Description | EFUSE_DIS_PAD_JTAG | EFUSE_DIS_USB_JTAG | EFUSE_JTAG_SEL_ENABLE | GPIO15 |
|-------------|--------------------|--------------------|-----------------------|--------|
| **JTAG Signal Source** | -                  | -                  | -                     | -      |
| USB Serial/JTAG Controller | `0`               | `0`                | `1`                   | `1`    |
| JTAG pins 2   | `0`               | `0`                | `1`                   | `0`    |
| JTAG is disabled | `1`              | `1`                | `1`                   | `Ignored` |

- Bold marks the default value and configuration.
- JTAG pins refer to MTDI, MTCK, MTMS, and MTDO.

---

**Footer:**
Espressif Systems
ESP32-C6 Series Datasheet v1.4

Submit Documentation Feedback