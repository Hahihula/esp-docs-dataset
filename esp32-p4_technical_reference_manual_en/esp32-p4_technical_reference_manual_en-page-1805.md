

```markdown
| Stage Three Input Data Byte Order¹ | LCD_CAM_LCD_DOUT_BYTE_SWIZZLE_MODE² | Stage Three Output Data Byte Order³ |
|---|---|---|
| 0 | B1,B0,B3,B2,B5,B4 | 
| 1 | B0,B2,B1,B3,B5,B4 | 
| 2 | B1,B0,B2,B4,B3,B5 | 
| 3 | B1,B2,B0,B4,B5,B3 | 
| 4 | B2,B0,B1,B5,B3,B4 | 
| 5 | B2,B1,B0,B5,B4,B3 | 

¹ B0 ~ B5 represent the bytes of the input data in stage three, i.e., the input data is arranged in a little-endian byte sequence. For example, when the valid data width of the input data is 16 bits, the original input data sequence B1,BOB3,B2B5,B4 is converted to B0,B1,B2,B3,B4,B5.
² Only the values listed in the table are valid. Other values may cause unexpected data errors.
³ The byte order of data that is ultimately transmitted to GPIO is determined by the “Stage Three Output Data Byte Order” and the bit width. For example, if the “Stage Three Output Data Byte Order” is B1,B0,B2,B4,B3,B5 and the transmitted data width is 16 bits, then the transmitted data byte order would be {B0,B1}{B4,B2}{B5,B3}. In this sequence, the data within each {} is in big-endian parallel format, and the data in each {} is in serial with the data in other {}. Data is transmitted from left to right. In this particular example, the data in {B0,B1} are in parallel with each other, while the data in {B0,B1} is in serial with the data in {B4,B2} and {B5,B3}. {B0,B1} is transmitted first.
```

### 38.3.5.2 Camera Data Format Control

When the Camera module receives data, configure the following registers to adjust the bit/byte order of the data sent to GDMA.

*   `LCD_CAM_CAM_2BYTE_EN`
    - 0: The data width of the Camera input is 8 bits.
    - 1: The data width of the Camera input is 16 bits.
*   `LCD_CAM_CAM_BIT_ORDER`
    - 0: Do not invert.
    - 1: Invert data bit order.
        *   Invert CAM_DATA_in[7:0] to CAM_DATA_in[0:7] in 8-bit mode.
        *   Invert CAM_DATA_in[15:0] to CAM_DATA_in[0:15] in 16-bit mode.
*   `LCD_CAM_CAM_BYTE_ORDER`
    - 0: Do not invert.
    - 1: Invert data byte order, only valid in 16-bit mode.

For the detailed configuration, see Table 38.3-4.
```