**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Section Header:**
2.5.2.12 REG_RD – Read from Peripheral Register

**Figure Caption and Instruction Type:**
- Figure 2.5-19.
- Instruction Type - REG_RD

**Operand Table with Descriptions for REG_RD:**

| Addr | Description |
|------|-------------|
| Low  | Register start bit number |
| High | Register end bit number |

**Description of REG_RD:**
The instruction reads up to 16 bits from a peripheral register into a general-purpose register:
- RO = REG[Addr][High:Low]
- In case of more than 16 bits being requested, i.e., High - Low + 1 > 16, then the instruction will return [Low+15:Low].

**Note for REG_RD:**
- This instruction can access registers in RTC_CNTL, RTC_IO, SENS, and RTC_I2C peripherals. Address of the register, as seen from the ULP coprocessor (addr_ulr), can be calculated from the address of the same register on the main bus (addr_bus) using:
  - addr_ulr = (addr_bus - DR_REG_RTCCNTL_BASE)/4
- The addr_ulr is expressed in 32-bit words, and value 0 maps onto the DR_REG_RTCCNTL_BASE as seen from the main CPU. Thus, 10 bits of address cover a 4096-byte range of peripheral register space.

**Section Header:**
2.5.2.13 REG_WR – Write to Peripheral Register

**Figure Caption and Instruction Type for REG_WR:**
- Figure 2.5-20.
- Instruction Type - REG_WR

**Operand Table with Descriptions for REG_WR:**

| Addr | Description |
|------|-------------|
| Data| Value to write, 8 bits |
| Low | Register start bit number |
| High | Register end bit number |

**Description of REG_WR:**
This instruction writes up to 8 bits from an immediate data value into a peripheral register.

**Footer Information:**
- Page Number: 321
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name: Espressif Systems

**Navigation Link:**
GoBack