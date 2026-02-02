**Chapter Title:**
Chapter 23 Pulse Count Controller (PCNT)

**Section Heading:**
23.3 Register Summary

**Body Text:**
The addresses in this section are relative to the PCNT base address provided in Table 3.3-6 in Chapter 3 System and Memory.

The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

**Table Headers:**
- Name
- Description
- Address
- Access

**Table Content (Partial):**

| Name | Description | Address       | Access |
|------|-------------|--------------|--------|
| PCNT_U0_CONF0_REG | Configuration register 0 for unit 0 | 0x3FF57000 | R/W    |
| PCNT_U1_CONF0_REG | Configuration register 0 for unit 1 | 0x3FF5700C | R/W    |
| ... | ... | ... | ... |

**Subsection Heading:**
Counter values

**Table Content (Partial):**

| Name | Description | Address       | Access |
|------|-------------|--------------|--------|
| PCNT_U0_CNT_REG | Counter value for unit 0 | 0x3FF57060 | RO     |
| PCNT_U1_CNT_REG | Counter value for unit 1 | 0x3FF57064 | RO     |
| ... | ... | ... | ... |

**Subsection Heading:**
Control registers

**Table Content (Partial):**

| Name | Description | Address       | Access |
|------|-------------|--------------|--------|
| PCNT_CTRL_REG | Control register for all counters | 0x3FF570B0 | R/W    |
| ... | ... | ... | ... |

**Footer:**
Espressif Systems  
454 ESP32 TRM (Version 5.6)  

**Link Texts:**
- GoBack
- Submit Documentation Feedback