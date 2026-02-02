**Chapter Title:**
Chapter 7 Reset and Clock

**Section Heading:**
7.4 Registers

**Body Text:**
The addresses in this section are relative to the SYSCON base address provided in Table 3.3-6 Peripheral Address Mapping in Chapter 3 System and Memory.

**Subsection with Register Description (Register 7.1):**

- **Title:** Register 7.1. SYSCON_SYCLK_CONF_REG (0x000)
  
  - **Binary Representation:**
    ```
    31       9        0
     (reserved)      0xO   Reset
    ```

  - **Description:**
    SYSCON_PRE_DIV_CNT Configures the divider value of CPU_CLK when the source of CPU_CLK is XTL_CLK or RC_FAST_CLK. The value range is 0x0 ~ 0x3FF. CPU_CLK = XTL_CLK (or RC_FAST_CLK) / (the value of this field +1). (R/W)

**Subsection with Register Description (Register 7.2):**

- **Title:** Register 7.2. SYSCON_XTAL_TICK_CONF_REG (0x0004)
  
  - **Binary Representation:**
    ```
    31       8        0
     (reserved)      0xO   Reset
    ```

  - **Description:**
    SYSCON_XTAL_TICK_NUM Configures the divider value of REF_TICK when the source of APB_CLK is XTL_CLK. The value range is 0x0 ~ 0xFF. REF_TICK = APB_CLK / (the value of this field +1). (R/W)

**Subsection with Register Description (Register 7.3):**

- **Title:** Register 7.3. SYSCON_PLL_TICK_CONF_REG (0x0008)
  
  - **Binary Representation:**
    ```
    31       8        0
     (reserved)      0xO   Reset
    ```

  - **Description:**
    SYSCON_PLL_TICK_NUM Configures the divider value of REF_TICK when the source of APB_CLK is PLL_CLK. The value range is 0x0 ~ 0xFF. REF_TICK = APB_CLK / (the value of this field +1). (R/W)

**Footer Information:**

- **Company:** Espressif Systems
- **Document Version and Type:** ESP32 TRM (Version 5.6)
- **Page Number:** 172

**Action Links:**
- Submit Documentation Feedback