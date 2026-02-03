**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Section Header:**
Register 6.36. IO_MUX_n_REG

**Body Text with Code Block:**
- **Continued from the previous page...**

**Subsection Title:**
IO_MUXFUN_DRV

**Subsection Body:**
Select the drive strength of the pin.

- GPIO17 and GPIO18
  - 0: ~5 mA
  - 1: ~20 mA
  - 2: ~10 mA
  - 3: ~40 mA

- Other GPIOs
  - 0: ~5 mA
  - 1: ~10 mA
  - 2: ~20 mA
  - 3: ~40 mA

**Subsection Title:**
IO_MUX_MCU_SEL

**Subsection Body:**
Select IO MUX function for this signal. O: Select Function 0; 1: Select Function 1, etc. (R/W)

**Subsection Title:**
IO_MUX_FILTER_EN

**Subsection Body:**
Enable filter for pin input signals. 1: Filter enabled; 0: Filter disabled. (R/W)

**Section Header with Subsection Number and Name:**
6.15.3 SDM Output Registers

**Body Text:**
The addresses in this section are relative to (GPIO base address provided in Table 4.3-3 in Chapter 4 System and Memory + OxFOO).

**Subsection Title:**
Register 6.37. GPIO_SIGMADELTA_n_REG

**Subsection Body with Code Block:**
- **(n: 0-7) (0x0000+4*n)**

**Binary Representation Table for GPIO_SDn_IN and GPIO_SDn_PRESCALE:**

| Bit | Description |
|-----|-------------|
| 31  |             |
| ... |             |
| 8   |             |
| 7   |             |
| 6   |             |
| 5   |             |
| 4   |             |
| 3   |             |
| 2   |             |
| 1   |             |
| 0   | Reset |

**Field Descriptions:**
- **GPIO_SDn_IN:** This field is used to configure the duty cycle of sigma delta modulation output. (R/W)
- **GPIO_SDn_PRESCALE:** This field is used to set a divider value to divide APB clock. (R/W)

**Footer Information:**
Espressif Systems
515 ESP32-S3 TRM (Version 1.7)