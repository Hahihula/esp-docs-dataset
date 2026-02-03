**Chapter Title:**
Chapter 15 Permission Control (PMS)

**Table Header:**
- Bus
- From World Configuration Registers
- Access

**Table Content for Table 15.3-2: Access Configuration to ROM**

| IBUS | Non-secure World | Secure World |
|------|------------------|--------------|
|      | PMS_CORE_X_IRAMO_PMS CONSTRAINT2_REG [20:18] B | X/W/R        |
|      | PMS_CORE_X_IRAMO_PMS CONSTRAINT1_REG [20:18] C | W/R          |
| DBUS | Secure World     | Non-secure World | PMS_CORE_XDRAMO_PMS CONSTRAINT1_REG [27:26] D | W/R          |

**Table Notes for Table 15.3-2:**
A) with access; O: without access
B) For example, configuring this field to Ob1 indicates CPU's IBUS is granted with instruction execution and read accesses but not write access to ROM from the Secure World.
C) For example, configuring this field to Ob01 indicates CPU’s DBUS is granted with read access but not write access to ROM from the Secure World.

**Subsection Title:**
15.3.2 SRAM

**Body Text for Subsection 15.3.2 SRAM:**
ESP32-S3's SRAM can be accessed by CPU’s instruction bus (IBUS) and data bus (DBUS) when configured.
Note:
- Permission for Secure World and Non-secure World can be configured independently.

Once configured, the configuration applies to both CPU0 and CPU1

**Subsection Title:**
15.3.2.1 Address

**Body Text for Subsection 15.3.2.1 Address:**
ESP32-S3's SRAM address and the address ranges accessible for IBUS and DBUS respectively are listed in Table 15.3-3.

**Table Header (for Table 15.3-3):**
- SRAM Block
- IBUS Starting Address Ending Address
- DBUS Starting Address Ending Address

**Table Content for Table 15.3-3:**

| SRAM | Block0 Internal SRAM0 | Block1 | Block2 | Block3 | Block4 | Block5 Internal SRAM1 | Block6 | Block7 | Block8 | Block9 | Block10 |
|------|-----------------------|--------|--------|--------|--------|--------------------|--------|--------|--------|--------|---------|
|      | 0x4037_0000          | -      | 0x4037_4000 | -     | 0x4037_FFFF | 0x4038_0000 | -       | 0x403A_0000 | -    | 0x403B_0000 | -      | 0x403C_0000 |
| IBUS Starting Address Ending Address | 0x4037_FFFF | 0x3FC8_8000 | 0x3FCC8_FFFF | 0x3FC9_0000 | 0x3FCA_FFFF | -       | 0x3FCB_FFFF | 0x3FCC_FFFF | 0x3FCD_FFFF | 0x3FCE_FFFF |
| DBUS Starting Address Ending Address | -          | -      | -     | -       | -       | 0x3FC9_0000 | 0x3FCA_FFFF | 0x3FCC_FFFF | 0x3FCD_FFFF | 0x3FCE_FFFF |

**Body Text for Subsection 15.3.2.1 Address Continued:**
Here, we will first introduce how to configure the permission to Internal SRAM0, Internal SRAM1, and Internal SRAM2, and also how to configure the Internal SRAM1 as CPU Trace memory.

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
685

**Action Links:**
- Submit Documentation Feedback