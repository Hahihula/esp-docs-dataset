**Title:**
Chapter 38 Pulse Count Controller (PCNT)

**Subtitle:**
38.4 Register Summary

**Body Text:**

The addresses in this section are relative to **Pulse Count Controller** base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

**Table Headers:**
- Name
- Description
- Address
- Access

**Table Content (Partial):**

| Name                          | Description                                                                                   | Address       | Access |
|-------------------------------|----------------------------------------------------------------------------------------------|---------------|--------|
| Configuration Register        |                                                                                               |               |        |
| PCNT_U0_CONFO_REG            | Configuration register 0 for unit 0                                                          | 0x0000        | R/W    |
| PCNT_U0_CONF1_REG            | Configuration register 1 for unit 0                                                          | 0x0004        | R/W    |
| ...                          | ...                                                                                           | ...           | ...    |

**Subsections:**

- **Status Register**
  - Counter value registers (e.g., PCNT_U0_CNT_REG, RO)
  
- **Interrupt Register**
  - Interrupt status and control registers
  
- **Version Register**
  - Version control register

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)