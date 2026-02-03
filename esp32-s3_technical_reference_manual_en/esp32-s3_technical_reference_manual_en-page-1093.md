**Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Subtitle:**
29.7 Registers

**Body Text:**
The addresses in this section are relative to LCD_CAM controller base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Table Title:**
Register 29.1. LCD_CAM_LCD_CLOCK_REG (0x0000)

| Address | Description |
|---------|-------------|
| 31      | LCD_CAM_LQK_EN |
| 30      | LCD_CAM_LQK_SEL |
| ...     | ...         |
| 4       | LCD_CAM_LQK_DIV_A |
| 5       | LCD_CAM_LQK_DIV_B |
| 6       | LCD_CAM_LQK_DIV_C |
| 7       | LCD_CAM_LQK_DIV_D |
| 8       | LCD_CAM_LQK_DIV_E |
| ...     | ...         |
| 0       | LCD_CAM_LQK_OUT_EDGE |

**Table Details:**
- **LCD_CAM_LCLK_CNT_N:** `f_LCD_PCLK = f_LCD_CLK / (LCD_CAM_LCLK_CNT_N + 1)` when `LCD_CAM_LCLK_EQU_SYSCLK` is O. Note: this field must not be configured to 0.
- **LCD_CAM_LCLK_EQU_SYSCLK:** `f_LCD_PCLK = f_LCD_CLK`
- **LCD_CAM_LCLK_IDLE_EDGE:** LCD_PCLK line high in idle; L: LCD_PCLK line low in idle
- **LCD_CAM_LCLK_OUT_EDGE:** LCD_PCLK is high in the first half clock cycle. O: LCD_PCLK is low in the first half clock cycle.
- **LCD_CAM_LCLKM_DIV_NUM:** Integral LCD clock divider value (R/W)
- **LCD_CAM_LCLKM_DIV_B:** Fractional clock divider numerator value
- **LCD_CAM_LCLKM_DIV_A:** Fractional clock divider denominator value

**Additional Information:**
- `LCD_CAM_LCLK_SEL`: Select LCD module source clock. O: clock source is disabled; 1: XTAL_CLK_2: PLL_D2_CLK, 3: PLL_F160M_CLK (R/W)
- **LCD_CAM_CLK_EN:** Set this bit to force enable the clock for all configuration registers. Clock gate is not used.

**Footer Information:**
Espressif Systems
Page number: 1093

**Link:**
Submit Documentation Feedback