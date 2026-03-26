

```markdown
2. Stage Two: Data color space conversion
   The YUV-RGB converter processes the data. If the YUV-RGB converter is disabled, the data remains unchanged at this stage.

3. Stage Three: Data post-processing
   The LCD module gets data from the YUV-RGB converter for post-processing and then transmits the data to GPIO.

Note:
The output data from the previous stage is the input data for the subsequent stage.
```

```markdown
The detailed configuration of each stage is described below.

Stage One: Data Preprocessing

At this stage, configure the following registers to adjust the bit width, bit order, and byte order of the data from GDMA.

• LCD_CAM_LCD_LCD_BYTE_MODE
  – 0: The data width of the LCD input from GDMA is 8 bits.
  – 1: The data width of the LCD input from GDMA is 16 bits.
  – 2: The data width of the LCD input from GDMA is 24 bits.

• LCD_CAM_LCD_BIT_ORDER
  – 0: Do not invert.
  – 1: Invert the input data bit order.

• LCD_CAM_LCD_BYTE_ORDER
  – 0: Do not invert.
  – 1: Invert data byte order, only valid in 16/24-bit modes.

For the detailed configuration, see Table 38.3-2.
```