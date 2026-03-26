
```markdown
Chapter 38 LCD and Camera Controller (LCD_CAM)

GoBack


• When HP_SYS_CLKRST_CAM_CLK_DIV_NUM = 1, N = 2.
• When HP_SYS_CLKRST_CAM_CLK_DIV_NUM = other value, N = HP_SYS_CLKRST_CAM_CLK_DIV_NUM.

b corresponds to the value of HP_SYS_CLKRST_CAM_CLK_DIV_NUMERATOR, and a to the value of
HP_SYS_CLKRST_CAM_CLK_DIV_DENOMINATOR.
• For integer divider, please clear HP_SYS_CLKRST_CAM_CLK_DIV_NUMERATOR and
HP_SYS_CLKRST_CAM_CLK_DIV_DENOMINATOR.
• For fractional divider, the value of HP_SYS_CLKRST_CAM_CLK_DIV_NUMERATOR should be smaller than
the value of HP_SYS_CLKRST_CAM_CLK_DIV_DENOMINATOR.



38.3.4 LCD_CAM Reset

LCD_CAM module has the following reset registers that can reset different parts of the module:
• HP_SYS_CLKRST_RST_EN_LCDCAM: Setting this register will reset the whole LCD_CAM module.
• LCD_CAM_LCD_RESET: Setting this register will reset the whole LCD module, including the LCD control
unit (LCD_Ctrl), the RGB/YUV Converter, and Async TX FIFO. Configuring this register will not affect the
Camera module.
• LCD_CAM_CAM_RESET: Setting this register will reset the whole Camera module, including the Camera
control unit (Camera_Ctrl), the RGB/YUV Converter, and Async RX FIFO. Configuring this register will not
affect the LCD module.
• LCD_CAM_LCD_AFIFO_RESET: Setting this register will reset the Async TX FIFO without affecting other
parts in the module. For example, setting this reset register every time the LCD finishes sending a frame
can prevent transmission errors of the previous frame from affecting the transmission of the next frame.
• LCD_CAM_CAM_AFIFO_RESET: Setting this register will reset the Async RX FIFO without affecting other
parts in the module. For example, setting this reset register every time the Camera finishes receiving a
frame can prevent transmission errors of the previous frame from affecting the receiving of the next
frame.



Notes:
• The reset register HP_SYS_CLKRST_RST_EN_LCDCAM is not self-clearing, meaning writing 1 enables the
reset, and writing 0 releases the reset.
• All the above reset registers, except for HP_SYS_CLKRST_RST_EN_LCDCAM, are self-clearing, meaning
that after writing 1, the hardware will generate a reset pulse and automatically clear the register.
• The module clocks LCD_CLK and CAM_CLK must be configured first before the module and FIFO are
reset.



38.3.5 LCD_CAM Data Format Control

38.3.5.1 LCD Data Format Control

When the data is transmitted by the LCD module, it undergoes three stages of processing:
1. Stage One: Data preprocessing
The LCD module processes the input data from GDMA and sends it to the YUV-RGB converter.



Espressif Systems      1802       ESP32-P4 TRM
Submit Documentation Feedback   PRELIMINARY
```