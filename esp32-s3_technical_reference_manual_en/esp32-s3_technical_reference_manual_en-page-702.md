Title: Chapter 15 Permission Control (PMS)

Subtitle: GoBack

Section Title:
15.6.6 Interrupt upon Unauthorized PIF Access Alignment

Body Text:

Access to all of ESP32-S3's modules/peripherals (excluding RTC FAST memory and SLOW memory) is word aligned.

ESP32-S3 can be configured to check the access alignment to all modules/peripherals, and trigger Interrupt upon non-word aligned access.
This interrupt corresponds to the CORE_m_PIF_PMS_MONITOR_VIOLATE_SIZE_INTR interrupt source described in Table 9.3-1 from Chapter 9 Interrupt Matrix (INTERRUPT).

Note that CPU can convert some non-word aligned access to word aligned access, thus avoiding triggering alignment interrupt.

Table Title:
Table 15.6-6 All Possible Access Alignment and their Results

Table Content:

| Accessed Address | Access Alignment       | Read   | Write |
|------------------|-------------------------|--------|-------|
| OX0             | Byte aligned           | INTR   | INTR  |
|                 | Half-word aligned      | INTR   | INTR  |
|                 | Word aligned           | √      | √     |
|                 | Byte aligned           |        |       |
| OX1             | Half-word aligned      | √      | INTR  |
|                 | Word aligned           | √      | INTR  |
|                 | Byte aligned           | INTR   | INTR  |
| OX2             | Half-word aligned      | INTR   | INTR  |
|                 | Word aligned           | √      | INTR  |
| OX3             | Half-word aligned      | INTR   | INTR  |
|                 | Word aligned           | INTR   | INTR  |

Table Title:
Table 15.6-7 Interrupt Registers for Unauthorized Access Alignment

Table Content:

| Registers                   | Bit    | Description                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------|
| PMS_CORE_m_PIF_PMS_MONITOR_4_REG | [1]    | Enables interrupt                                                                                    |
|                             | [0]    | Clears interrupt signal and logged information                                                       |
|                             |        | Stores the world the CPU was in when the unauthorized access happened. 0b01: Secure World; 0b10: Non-secure World |
| PMS_CORE_m_PIF_PMS_MONITOR_5_REG | [2:1] | Stores the unauthorized access type. 0: byte aligned; 1: half-word-aligned; 2: word aligned       |
|                             | [0]    | Stores the interrupt status. 0: no interrupt; 1: interrupt                                          |
| PMS_CORE_m_PIF_PMS_MONITOR_6_REG | [31:0]| Stores the address of the unauthorized access                                                        |

Footer:
Espressif Systems
702 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback