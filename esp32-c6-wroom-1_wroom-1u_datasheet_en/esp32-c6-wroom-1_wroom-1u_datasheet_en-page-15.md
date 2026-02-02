**Title: Boot Configurations**

---

### Table 4-6. USB Serial/JTAG ROM Message Printing Control

| USB Serial/JTAG | EFUSE_DIS_USB_SERIAL_JTAG | EFUSE_DIS_USB_SERIAL_ROM_PRINT |
|------------------|---------------------------|--------------------------------|
| ROM Code Printing | Enabled                   | 0                               |
|                   | Disabled                  | 1                               |

**Note:** Bold marks the default value and configuration.

2. **EFUSE_DIS_USB_SERIAL_JTAG**: controls whether to disable USB Serial/JTAG

---

### Section: JTAG Signal Source Control (4.4)

The strapping pin GPIO15 can be used to control the source of JTAG signals during the early boot process.
This pin does not have any internal pull resistors and the strapping value must be controlled by the external circuit that cannot be in a high impedance state.

As Table 4-7 shows, GPIO15 is used in combination with EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_JTAG_SEL_ENABLE.

---

### Table 4-7. JTAG Signal Source Control

| JTAG Signal Source | EFUSE_DIS_PAD_JTAG | EFUSE_DIS_USB_JTAG | EFUSE_JTAG_SEL_ENABLE | GPIO15 |
|--------------------|---------------------|--------------------|------------------------|--------|
| USB Serial/JTAG Controller | 0                   | 0                  | 1                      | 1      |
| JTAG pins           | 0                   | 0                  | 1                      | 0      |
| JTAG                | 0                   | 1                  | 1                      | Ignored|
|                     | 1                   |                    |                        |        |

**Note:** Bold marks the default value and configuration.

2. **JTAG pins**: refer to MTDI, MTCK, MTMS, and MTDO

---

### Section: Chip Power-up and Reset (4.5)

Once the power is supplied to the chip, its power rails need a short time to stabilize.
After that, CHIP PU – the pin used for power-up and reset - is pulled high to activate the chip.

For information on CHIP PU as well as power-up and reset timing,
see Figure 4-2 and Table 4-8:

---

**Figure 4-2. Visualization of Timing Parameters for Power-up and Reset**

[Image depicting voltage levels over time with labels such as VDDA3P3, VDDPST1, VDDPST2, VDDA1, VDDA2, CHIP PU, t_STBL, t_RST]

---

**Footer:**
Espressif Systems
Page 15 ESP32-C6-WROOM-1 & WROOM-1U Datasheet v1.4

Submit Documentation Feedback