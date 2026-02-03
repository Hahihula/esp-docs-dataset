**Chapter Title:**
Chapter 17 System Registers (SYSTEM)

**Register Information and Descriptions:**

- **Register Name:** SYSTEM_BT_LPCK_DIV_FRAC_REG (0x002C)
  - **Field Description:**
    - `31 to 29`: Reserved.
    - `28 to 26`: SYSTEM_LPCLK_RTC_EN
    - `25 to 24`: SYSTEM_LPCLK_XTAL32K
    - `23 to 0`: SYSTEM_LPCLK_SLOW_CLK
    - `22 to 19`: SYSTEM_LPCLK_SEL_RTC
    - `18 to 16`: SYSTEM_LPCLK_SEL_8M
    - `15 to 14`: SYSTEM_LPCLK_SEL_XTAL
    - `13 to 0`: SYSTEM_LPCLK_SEL_XTAL32K

- **Field Details:**
  - `SYSTEM_LPCLK_SLOW_CLK (R/W)`: Set this bit to select RTC_SLOW_CLK as the low-power clock.
  - `SYSTEM_LPCLK_SEL_8M (R/W)`: Set this bit to select RC_FAST_CLK div n as the low-power clock.

- **Register Name:** SYSTEM_LPCLK_SEL_XTAL
  - Description: Set this bit to select XTAL_CLK clock as the low-power clock. (R/W)

- **Register Name:** SYSTEM_LPCLK_SEL_XTAL32K
  - Description: Set this bit to select XTAL32K_CLK clock as the low-power clock.

- **Register Name:** SYSTEM_LPCLK_RTC_EN
  - Description: Set this bit to enable the LOW_POWER_CLK clock. (R/W)

**Register Information and Descriptions for another register:**

- **Register Name:** SYSTEM_CPU_INTR_FROM_CPU_O_REG (0x0030)
  - `Field Description:`
    - `31 to 29`: Reserved.
    - `28 to 26`: SYSTEM_CPU_INTR_FROM_CPU
    - `25 to 24`: SYSTEM_CPU_INTR
    - `23 to 0`: SYSTEM_CPU_INTR_0

- **Field Details:**
  - `SYSTEM_CPU_INTR_0 (R/W)`: Set this bit to generate CPU interrupt. This bit needs to be reset by software in the ISR process.

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback