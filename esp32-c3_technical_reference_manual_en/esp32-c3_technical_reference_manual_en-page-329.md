

```markdown
| Registers | Bit | Description |
|-----------|-----|-------------|
| PMS_CORE_O_IRAMO_PMS_MONITOR_1_REG | [0] | Clears interrupt signal |
|  | [1] | Enables interrupt |
|  | [0] | Stores interrupt status of unauthorized IBUS access |
| PMS_CORE_O_IRAMO_PMS_MONITOR_2_REG | [1] | Stores the access direction. 1: write; 0: read. |
|  | [2] | Stores the instruction direction. 1: load/store; 0: instruction execution. |
|  | [4:3] | Stores the privileged mode the CPU was in when the unauthorized IBUS access happened. Ob01: privileged environment; Ob10: unprivileged environment |
|  | [28:5] | Stores the address that CPU's IBUS was trying to access unauthorized. |

## 14.7.2 Interrupt upon Unauthorized DBUS Access

ESP32-C3 can be configured to trigger interrupts when DBUS attempts to access internal ROM and SRAM without configured permission and log the information about this unauthorized access. Note that, once this interrupt is enabled, it's enabled for all internal ROM and SRAM memory, and cannot be only enabled for a certain address field. This interrupt corresponds to the PMS_DBUS_VIO_INTR interrupt source described in Table 8.3-1 from Chapter 8 Interrupt Matrix (INTERRUPT).

Table 14.7-2. Interrupt Registers for Unauthorized DBUS Access

| Registers | Bit | Description |
|-----------|-----|-------------|
| PMS_CORE_O_DRAMO_PMS_MONITOR_1_REG | [0] | Clears interrupt signal |
|  | [1] | Enables interrupt |
|  | [0] | Stores interrupt status of unauthorized DBUS access |
| PMS_CORE_O_DRAMO_PMS_MONITOR_2_REG | [1] | Flags atomic access. 1: atomic access; 0: not atomic access. |
|  | [3:2] | Stores the privileged mode the CPU was in when the unauthorized DBUS access happened. Ob01: privileged environment; Ob10: unprivileged environment |
|  | [25:4] | Stores the address that CPU's DBUS was trying to access unauthorized. |
| PMS_CORE_O_DRAMO_PMS_MONITOR_3_REG | [0] | Stores the access direction. 1: write; 0: read. |
|  | [25:4] | Stores the byte information of the unauthorized DBUS access. |
```