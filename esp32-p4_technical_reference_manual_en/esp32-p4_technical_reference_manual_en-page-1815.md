

```markdown
## 38.7 Registers

The addresses in this section are relative to LCD_CAM base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 38.1. LCD_CAM_LCD_CLOCK_REG (0x0000)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | LCD_CAM_CLK_EN                                                              |
| 30  | (reserved)                                                                  |
| 29-0| 0x0                                                                          |

LCD_CAM_LCD_CLKCNT_N Determines the frequency of the LCD pixel clock LCD_PCLK together with LCD_CAM_LCD_EQU_SYSCLK.
When LCD_CAM_LCD_CLK_EQU_SYSCLK = 0,
f_LCD_PCLK = f_LCD_CLK / (LCD_CAM_LCD_CLKCNT_N + 1)
Note: this field must not be configured to 0.
(R/W)

LCD_CAM_LCD_CLK_EQU_SYSCLK Determines the frequency of the LCD pixel clock LCD_PCLK together with LCD_CAM_LCD_CLK_EQU_SYSCLK.
0: f_LCD_PCLK = f_LCD_CLK / (LCD_CAM_LCD_CLKCNT_N + 1)
1: f_LCD_PCLK = f_LCD_CLK
(R/W)

LCD_CAM_LCD_CK_IDLE_EDGE Indicates the level of LCD_PCLK in idle state.
0: LCD_PCLK is low.
1: LCD_PCLK is high.
(R/W)

LCD_CAM_LCD_CK_OUT_EDGE Indicates the level of LCD_PCLK in the first half clock cycle.
0: LCD_PCLK is low.
1: LCD_PCLK is high.
(R/W)

LCD_CAM_CLK_EN Set this bit to force enable the clock for all configuration registers. Clock gate is not used. (R/W)
```