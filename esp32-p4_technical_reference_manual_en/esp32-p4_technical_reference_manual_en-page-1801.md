

```markdown
- When `LCD_CAM_LCD_CLK_EQU_SYSCLK = 0`, MO = `LCD_CAM_LCD_CLKCNT_N + 1`.

Notes:
*   `LCD_CAM_LCD_CLKCNT_N` must not be configured as 0.
*   Using fractional divider may introduce clock jitters. In case `LCD_CLK` and `LCD_PCLK` can not be generated from `PLL_F160M_CLK` by integer divider, `APLL_CLK` can be used as the clock source. For more information, please refer to Chapter 10 Reset and Clock.

### 38.3.3.2 Camera Clock

The clocks used in the Camera module are generated from clock sources by the CAM_Clock Generator, see Figure 38.3-3. The clocks include:

*   Master clock: `CAM_CLK`, master clock output from the Camera module, divided from the clock sources.
*   Pixel clock: `CAM_PCLK`, clock input from camera slave.

`HP_SYS_CLKRST_CAM_CLK_EN` is used to enable the `CAM_CLK_SRC` (the clock source), and `HP_SYS_CLKRST_CAM_CLK_SRC_SEL` is used to select `CAM_CLK_SRC` from one of the following clock sources:

*   0: `XTAL_CLK`
*   1: `PLL_F160M_CLK`
*   2: `APLL_CLK`
*   3: Disable camera clock source

![Figure 38.3-3. Camera Clock](image)

The following formula shows the relation between the frequencies of `CAM_CLK` (`f_CAM_CLK`) and the divider’s clock source (`f_CAM_CLK_SRC`):

```latex
f_{\text{CAM_CLK}} = \frac{f_{\text{CAM_CLK\_SRC}}}{N + \frac{b}{a}}
```

*N* is an integer value between 2 and 256. The value of *N* corresponds to the value of `HP_SYS_CLKRST_CAM_CLK_DIV_NUM` as follows:

*   When `HP_SYS_CLKRST_CAM_CLK_DIV_NUM = 0`, N = 256.
```