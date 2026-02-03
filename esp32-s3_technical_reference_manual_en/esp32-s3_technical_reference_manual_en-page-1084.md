**Chapter Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Note Section:**
If only one byte of data is sent out each time, LCD_Data_out[7:0] is valid, while LCD_Data_out[15:8] is invalid.

**Section Heading:**
29.3.5.2 Camera Data Format Control

**Body Text:**
When the camera module is used to receive data, the bit/byte order of the data to DMA can be adjusted by configuring:

- **LCD_CAM_CAM_2BYTE_EN**
  - 1: Camera input data is in 16-bit mode.
  - 0: Camera input data is in 8-bit mode.

- **LCD_CAM_CAM_BIT_ORDER**
  - Change data bit order:
    * Change CAM_DATA_in[7:0] to CAM_DATA_in[0:7] in 8-bit mode.
    * Change CAM_DATA_in[15:0] to CAM_DATA_in[0:15] in 16-bit mode.

- **LCD_CAM_CAM_BYTE_ORDER**
  - Do not change the bit order:
    * Invert data byte order, only valid in 16-bit mode.
    * Do not invert.

**Subsection Heading and Table Reference:**
For the detailed configuration, see Table 29.3-3

**Table Title:**
Table 29.3-3 CAM Data Format Control

| RX Data | LCD_CAM_CAM_2BYTE_EN | LCD_CAM_CAM_BIT_ORDER | LCD_CAM_CAM_BYTE_ORDER | Data to DMA |
|---------|-----------------------|------------------------|-------------------------|-------------|
| {B0}{B1}{B2}{B3} | 0                     | 0                      | O                       | B0,B1,B2,B3 |
|                   | 1                     | 1                      | O                       | B0',B1',B2',B3' |
| {B1,BO}{B3,B2}   |                           |                        |                         | B0,B1,B2,B3 |
|                   | 1                     | 1                      |                          | B1,BO,B3,B2 |

**Table Footnotes:**
1 In RX data, the bits in {} are in big-endian, and are in parallel with each other, while the data of {} is in serial with the data of other {}. Data is received from left to right. Take {BO}{B1}{B2}{B3} as an example. The bits in {BO} are in parallel with each other, but are in serial with the bits in {B1}[B2]{B3}. {BO} is received first.
2 Only the configuration listed in the table is valid. Other configuration may cause unexpected data errors.
3 BO ~ B3 represent the bytes of the data to DMA, from low address to high address.
4 In the data to DMA, Bn[7:0] = Bn[0:7] (n = 0,1,2,3).

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version and Page Number:**
ESP32-S3 TRM (Version 1.7)
Page number not visible in the image provided.

(Note: The text content is transcribed as it appears from top to bottom without any additional interpretation or formatting beyond what was requested.)