**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**Section Header:**
GoBack

**Body Text with Subsections and Figures:**

---

### 1.4.13 REG_RD – Read from Peripheral Register

When working in master mode, RTC_I2C samples the SDA input on the negative edge of SCL.

- **Figure Caption:** Figure 1.4-16. Instruction Type — REG_RD
- **Table:**
  - Address bits (from top to bottom): 31, 28, 27, 23, 22, 18, 9, 0

#### Operands:
- **Addr:** Register address, expressed in 32-bit words.
- **High:** Register end bit number
- **Low:** Register start bit number

**Description:**
The instruction prompts a read of up to 16 bits from a peripheral register into a general-purpose register RO:

- `RO = REG[Addr][High:Low]`

In case of more than 16 bits being requested, i.e., High - Low + 1 > 16, then the instruction will return [Low+15:Low].

**Note:** 
- This instruction can access registers in RTC_CNTL, RTC_IO, SENS and RTC_I2C peripherals. The address of the register, as seen from the ULP coprocessor, can be calculated from the address of the same register on the DPORT bus, as follows:
  - `addr_ulp = (addr_dport - DR_REG_RTCNTL_BASE)/4`
- The addr_ulp is expressed in 32-bit words (not in bytes), and value 0 maps onto the DR_REG_RTCNTL_BASE (as seen from the main CPUs). Thus, 10 bits of address cover a 4096-byte range of peripheral register space, including regions DR_REG_RTCNTL_BASE, DR_REG_RTCIO_BASE, DR_REG_SENS_BASE and DR_REG_RTC_I2C_BASE.

---

### 1.4.14 REG_WR – Write to Peripheral Register

When working in master mode, RTC_I2C samples the SDA input on the negative edge of SCL.

- **Figure Caption:** Figure 1.4-17. Instruction Type — REG_WR
- **Table:**
  - Address bits (from top to bottom): 31, 28, 27, 23, 22, 18, 9, Data

#### Operands:
- **Addr:** Register address, expressed in 32-bit words.
- **High:** Register end bit number
- **Low:** Register start bit number
- **Data:** Value to write, 8 bits

**Description:**
The instruction prompts the writing of up to 8 bits from an immediate data value into a peripheral register.

- `REG[Addr][High:Low] = Data`

---

**Footer Information:**
Espressif Systems  
39  
ESP32 TRM (Version 5.6)  
Submit Documentation Feedback