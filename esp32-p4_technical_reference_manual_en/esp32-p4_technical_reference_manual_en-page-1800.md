

```markdown
HP_SYS_CLKRST_LCD_CLK_EN is used to enable LCD_CLK_SRC (the clock source), and  
HP_SYS_CLKRST_LCD_CLK_SRC_SEL is used to select LCD_CLK_SRC from one of the following clock sources:

- 0: XTAL_CLK
- 1: PLL_F160M_CLK
- 2: APLL_CLK
- 3: Disable LCD clock source

![Figure 38.3-2. LCD Clock](image)

The following formula shows the relation between the frequency of LCD_CLK (f_LCD_CLK) and LCD_CLK_SRC (f_LCD_CLK_SRC):

$$ f_{LCD\_CLK} = \frac{f_{LCD\_CLK\_SRC}}{N + \frac{b}{a}} $$

The values of N, a, and b are related to HP_SYS_CLKRST_LCD_CLK_DIV_NUM,  
HP_SYS_CLKRST_LCD_CLK_DIV_NUMERATOR, and HP_SYS_CLKRST_LCD_CLK_DIV_DENOMINATOR. Specifically,

- When HP_SYS_CLKRST_LCD_CLK_DIV_NUM = 0, N = 1. The values of a and b do not take effect. The divider is always 1.
- When HP_SYS_CLKRST_LCD_CLK_DIV_NUM >= 1, N = HP_SYS_CLKRST_LCD_CLK_DIV_NUM + 1.

    - For integer divider, please clear HP_SYS_CLKRST_LCD_CLK_DIV_NUMERATOR and  
      HP_SYS_CLKRST_LCD_CLK_DIV_DENOMINATOR.
    - For fractional divider, b = HP_SYS_CLKRST_LCD_CLK_DIV_NUMERATOR, a =  
      HP_SYS_CLKRST_LCD_CLK_DIV_DENOMINATOR. The value of  
      HP_SYS_CLKRST_LCD_CLK_DIV_NUMERATOR should be smaller than the value of  
      HP_SYS_CLKRST_LCD_CLK_DIV_DENOMINATOR.

The following formula shows the relation between the frequencies of LCD_PCLK (f_LCD_PCLK) and LCD_CLK (f_LCD_CLK):

$$ f_{LCD\_PCLK} = \frac{f_{LCD\_CLK}}{MO} $$

MO is determined by LCD_CAM_LCD_CLK_EQU_SYSCLK and LCD_CAM_LCD_CLKCNT_N, specifically:

- When LCD_CAM_LCD_CLK_EQU_SYSCLK = 1, MO = 1.
```