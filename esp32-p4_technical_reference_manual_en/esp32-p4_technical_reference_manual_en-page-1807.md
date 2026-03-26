

```markdown
Chapter 38 LCD and Camera Controller (LCD_CAM)
GoBack

* In YUV422 mode, the LCD sends (or the camera receives) the data as follows:

| Y₁ | U₁ | Y₂ | V₂ | Y₃ | U₃ | V₄ | Y₅ | U₅ | V₆ | Y₇ | U₇ | V₈ |

* In YUV420 mode, the LCD and the camera do not participate in format conversion.

* In YUV411 mode, the LCD sends (or the camera receives) the data as follows:

| Y₁ | U₁ | Y₂ | V₂ | Y₃ | V₃ | Y₄ | U₅ | V₆ | Y₇ | V₇ | Y₈ |
```

## 38.3.6.2 Format Conversion Configuration

The configuration process for the format conversion in the Camera module is almost identical to that in the LCD module. Therefore, we will illustrate the process using the example of format conversion in the LCD module.

1. Enable YUV-RGB format converter by setting `LCD_CAM_LCD_CONV_ENABLE`.

2. Configure the valid bit width of the input data by configuring `LCD_CAM_LCD_CONV_MODE_8BITS_ON`:
   * 0: The valid bit width is 16 bits.
   * 1: The valid bit width is 8 bits.

3. Configure the valid bit width of the output data:
   * For the format conversion in the Camera module, the valid bit width of the output data is equal to that of the input data.
   * For the format conversion in the LCD module, when `LCD_CAM_LCD_WIRE_MODE` is:
     - 2: The valid bit width of the format converter’s output data is 24 bits.
     - Other value: The valid bit width of the format converter’s output data is equal to that of the input data.

4. Select the standard by configuring `LCD_CAM_LCD_CONV_PROTOCOL_MODE`:
   * 0: BT601 standard
   * 1: BT709 standard

5. Configure the conversion mode:
   * In 24-bit output mode:
```