**Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Subtitle:**
GoBack

**Section Title:**
29.3.5 LCD_CAM Data Format Control

**Subsection Title:**
29.3.5.1 LCD Data Format Control

**Body Text:**

When the LCD module is used to send data, the bit/byte order of the data from DMA can be adjusted by configuring:

- **LCD_CAM_LCD_2BYTE_EN**
  - 0: LCD output data is in 8-bit mode.
  - 1: LCD output data is in 16-bit mode.

- **LCD_CAM_LCD_BIT_ORDER**
  - Change data bit order:
    * Change LCD_DATA_out[7:0] to LCD_DATA_out[0:7] in 8-bit mode.
    * Change LCD_DATA_out[15:0] to LCD_DATA_out[0:15] in 16-bit mode.

- **LCD_CAM_LCD_BYTE_ORDER**
  - Invert data byte order, only valid in 16-bit mode:
    * Do not invert the bit order. 

- **LCD_CAM_LCD_8BITS_ORDER**
  - Swap every two data bytes, valid in 8-bit mode.
  - Data is sent out from left to right.

**Table Title:**
Table 29.3-2. LCD Data Format Control

| Data DMA | from | LCD_CAM_LCD_2BYTE_EN | LCD_CAM_LCD_BIT_ORDER | LCD_CAM_LCD_BYTE_ORDER | LCD_CAM_LCD_8BITS_ORDER | TX Data |
|----------|------|-----------------------|------------------------|-------------------------|---------------------------|--------|
| 0        |      |                       |                        |                         |                           | {B0}{B1}{B2}{B3} |
| B0,B1,B2,B3 |     |                       |                        |                         |                           | {B0}{B1}{B2}{B3} |
|          | 0    |                       |                        |                         |                           | {BO}{B1}{B2}{B3} |
|          |      |                       |                        |                         |                           | {BO}{B1}{B2}{B3} |
|          | 1    |                       |                        |                         |                           | {BO}{B1}{B2}{B3} |

**Footnotes:**
1. BO ~ B3 represent the bytes of the data from DMA, from low address to high address.
2. Only the configuration listed in the table is valid. Other configuration may cause unexpected data errors.

**Additional Information about TX Data:**

- In TX data, the bits in {} are in big-endian, and are in parallel with each other; while the data of {} is in serial with the data of other {}.
- Data is sent out from left to right. Take {BO}[B1]{B2}{B3} as an example.

**Explanation:**
In TX data:
- Bn[7:0] = Bn[0:7] (n = 0,1,2,3).

**Footer Information:**

Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback