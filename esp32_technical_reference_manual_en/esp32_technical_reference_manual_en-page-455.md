**Chapter Title:**
Chapter 23 Pulse Count Controller (PCNT)

**Table of Registers and Their Descriptions**

| Name                   | Description                                    | Address       | Access |
|------------------------|-------------------------------------------------|---------------|--------|
| PCNT_INT_RAW_REG      | Raw interrupt status                            | 0x3FF57080   | RO     |
| PCNT_INT_ST_REG       | Masked interrupt status                         | 0x3FF57084   | RO     |
| PCNT_INT_ENA_REG      | Interrupt enable bits                          | 0x3FF57088   | R/W    |
| PCNT_INT_CLR_REG      | Interrupt clear bits                            | 0x3FF5708C   | WO     |
| PCNT_Um_STATUS_REG    | Indicate the status of counter                  | 0x3FF57090   | RO     |

**Subsection Title:**
23.4 Registers

**Body Text:**
The addresses in this section are relative to the PCNT base address provided in Table 3.3-6 in Chapter 3 System and Memory. The absolute register addresses are listed in Section **23.3 Register Summary**.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

**Footer:**
Espressif Systems
455 ESP32 TRM (Version 5.6)
Submit Documentation Feedback