**Title: Chapter 17 System Registers (SYSTEM)**

**Subtitle: Register 17.3. SYSTEM_CPU_PER_CONF_REG (0x0010)**

**Binary Representation Table**
- Columns labeled from right to left as follows:
  - SYSTEM_CPU_WAIT_MODEFORCE_ON
  - SYSTEM_CPU_WAIT_DELAY_NUM
  - SYSTEM_PLL_FREQ_SEL
  - SYSTEM_CPUUPERIOD_SEL
  - (reserved)
  - SYSTEM_CPU WAIT MODE FORCE ON
  - SYSTEM_CPU WAIT DELAY NUM
  - SYSTEM_PLL FREQ SEL
  - SYSTEM_CPUUPERIOD SEL

**Hexadecimal Values:**
- The binary representation is shown with hexadecimal values on the right side, starting from bit position '0' to '31'.

**Field Descriptions and Functions:**

1. **SYSTEM_CPUPERIOD_SEL**: Set this field to select the CPU clock frequency.
   - Access type (R/W)

2. **SYSTEM_PLL_FREQ_SEL**: Set this bit to select the PLL clock frequency.
   - Access type (R/W)

3. **SYSTEM_CPU_WAIT_MODEFORCE_ON**: Set this bit to force on the clock gate of CPU wait mode after executing the WAITI instruction, allowing for reduced power consumption by keeping the clock off until interrupts occur or a WAITI instruction is executed again.

4. **SYSTEM_CPU_WAIT_DELAY_NUM**: Sets the number of delay cycles to turn off the CPU clock gate when entering wait mode due to a WAITI instruction.
   - Access type (R/W)

**Footer:**
- "Espressif Systems"
- Page Number 830
- Document Title ESP32-S3 TRM (Version 1.7)
- Link for submitting documentation feedback