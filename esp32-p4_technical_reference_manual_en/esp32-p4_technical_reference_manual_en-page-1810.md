

```markdown
Chapter 38 LCD and Camera Controller (LCD_CAM)

Figure 38.3-5. LCD Timing (RGB Format)


Note:
When configuring the parameters shown in the figures above, please note that the parameter is equal to the register value + 1. For example, if the expected VSYNC width is 1, then please configure LCD_CAM_LCD_VSYNC_WIDTH to 0.
For more information, see the register description.


38.3.7.2 LCD Timing (I8080/MOTO6800 Format)

Figure 38.3-6 shows the LCD timing sequence in I8080/MOTO6800 format.

Figure 38.3-6. LCD Timing (I8080/MOTO6800 Format)


38.4 Interrupts

ESP32-P4's LCD_CAM can generate the following interrupt signal that will be sent to the Interrupt Matrix.
• LCD_CAM_INTR

The following internal interrupt sources from LCD_CAM can generate LCD_CAM_INTR:
• LCD_CAM_CAM_HS_INT: Triggered when the Camera module receives lines more than or equal to the value of LCD_CAM_CAM_LINE_INT_NUM + 1.
• LCD_CAM_CAM_VSYNC_INT: Triggered when the Camera module receives a whole frame.

Espressif Systems
Submit Documentation Feedback
ESP32-P4 TRM
PRELIMINARY
```