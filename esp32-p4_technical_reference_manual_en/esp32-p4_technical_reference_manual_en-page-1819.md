

```markdown
Register 38.3. LCD_CAM_LCD_USER_REG (0x0014)

Continued from the previous page...

LCD_CAM_LCD_BYTE_ORDER Configures whether to invert the byte order of the LCD input data.
O: Do not invert.
1: Invert data byte order, only valid in 16/24-bit mode.
(R/W)

LCD_CAM_LCD_DOUT Configures the LCD DOUT phase.
O: Disable.
1: The LCD module sends data in RGB/I8080 format.
(R/W)

LCD_CAM_LCD_DUMMY Configures the LCD DUMMY phase.
O: Disable.
1: Enable the DUMMY phase when LCD initiates.
(R/W)

LCD_CAM_LCD_CMD Configures the LCD CMD phase.
O: Disable.
1: The LCD module sends commands.
(R/W)

LCD_CAM_LCD_START When set to 1, the LCD module starts transmitting data. (R/W)

LCD_CAM_LCD_RESET When set to 1, the LCD module is reset. (WO)

LCD_CAM_LCD_DUMMY_CYCLELEN Configures DUMMY cycles. DUMMY cycles = this value + 1.
(R/W)

LCD_CAM_LCD_CMD_2_CYCLE_EN Configures the number of cycles of the Command phase.
O: One cycle.
1: Two cycles.
(R/W)
```