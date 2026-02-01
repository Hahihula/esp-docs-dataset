**Title: Boot Configurations**

---

### **3.2 ROM Messages Printing Control**

During the boot process, ROM message printing is enabled if LP_AON_STORE4_REG[0] is 0 (default), and disabled if LP_AON_STORE4_REG[0] is 1. When ROM message printing is enabled, the messages can be printed to:

- **(Default) UARTO** and USB Serial/JTAG controller
- USB Serial/JTAG controller

EFUSE_UART_PRINT_CONTROL, LP_AON_STORE4_REG[0], and GPIO8 control ROM messages printing to UARTO as shown in Table 3-4.

**Table Title: Table 3-4. UARTO ROM Message Printing Control**

| UARO ROM Message Printing | LP_AON_STORE4_REG[0] | EFUSE_UART_PRINT_CONTROL | GPIO8 |
|---------------------------|----------------------|--------------------------|-------|
| Enabled                   | 0                    | Ignored                  | 0     |
|                           |                      |                         |       |
| Disabled                  | 1                    |                        | 3     |

**Note:** Bold marks the default value and configuration.

EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT controls the printing to USB Serial/JTAG controller as shown in Table 3-5.

**Table Title: Table 3-5. USB Serial/JTAG ROM Message Printing Control**

| USB Serial/JTAG ROM Message | LP_AON_STORE4_REG[0] | EFUSE_DIS_USB_SERIAL_JTAG_PRINTControl |
|------------------------------|----------------------|----------------------------------------|
| Enabled                      | 0                    | Ignored                                |
| Disabled                     | 1                    | Ignored                                |

**Note:** Bold marks the default value and configuration.

---

### **3.3 JTAG Signal Source Control**

The strapping pin GPIO25 can be used to control the source of JTAG signals during the early boot process. This pin does not have any internal pull resistors and the strapping value must be controlled by the external circuit that cannot be in a high impedance state.

As Table 3-6 shows GPIO25 is used in combination with EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_JTAG_SEL_ENABLE. 

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

ESP32-H2 Series Datasheet v1.2