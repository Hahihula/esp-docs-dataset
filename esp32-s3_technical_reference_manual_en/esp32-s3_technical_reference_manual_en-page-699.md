**Chapter Title:**
Chapter 15 Permission Control (PMS)

**Body Text:**

- All instruction execution or read attempts will be responded with 0 (for internal memory) or Oxdeadbeaf (for external memory)
- All write attempts will fail

An interrupt will be triggered (when enabled). See details below.

Note that:
- All permission control related interrupts described in this section can be independently configured for CPU0 and CPU1.
- Only the information of the first interrupt is logged. Therefore, it’s advised to handle interrupt signals and clear interrupts in-time, so the information of next interrupt can be logged correctly.

**Subsection Title:**
15.6.1 Interrupt upon Unauthorized IBUS Access

ESP32-S3 can be configured to trigger interrupts when IBUS attempts to access internal ROM and SRAM without configured permission, and log the information about this unauthorized access. Note that, once this interrupt is enabled, it’s enabled for all internal ROM and SRAM memory, and cannot be only enabled for a certain address field. This interrupt corresponds to the CORE_m_IRAMO_PMS_MONITOR_VIOLATE_INTR interrupt source described in Table 9.3-1 from Chapter 9 Interrupt Matrix (INTERRUPT).

**Table Title:**
Table 15.6-1. Interrupt Registers for Unauthorized IBUS Access

| Registers | Bit | Description |
|-----------|-----|-------------|
| PMS_CORE_m_IRAMO_PMS_MONITOR_1_REG | [0] | Clears interrupt signal |
| | [1] | Enables interrupt |
| | [0] | Stores interrupt status of unauthorized IBUS access |
| PMS_CORE_m_IRAMO_PMS_MONITOR_2_REG | [1] | Stores the access direction. 1: write; 0: read. |
| | [2] | Stores the instruction direction. 1: load/store; 0: instruction execution. |
| | (4:3) | Stores the world the CPU was in when the unauthorized IBUS access happened. Ob01: Secure World; Ob10: Non-Secure World |
| | (28:5) | Stores the address that CPU’s IBUS was trying to access unauthorized. |

**Subsection Title:**
15.6.2 Interrupt upon Unauthorized DBUS Access

ESP32-S3 can be configured to trigger interrupts when DBUS attempts to access internal ROM and SRAM without configured permission, and log the information about this unauthorized access. Note that, once this interrupt is enabled, it’s enabled for all internal ROM and SRAM memory, and cannot be only enabled for a certain address field. This interrupt corresponds to the CORE_m_DRAMO_PMS_MONITOR_VIOLATE_INTR interrupt source described in Table 9.3-1 from Chapter 9 Interrupt Matrix (INTERRUPT).

**Footer:**
Espressif Systems  
699 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback