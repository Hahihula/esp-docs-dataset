

```markdown
Table 38.3-4. Camera Data Format Control

| RX Data Order¹ | LCD_CAM_CAM _2BYTE_EN | LCD_CAM_CAM _BIT_ORDER² | LCD_CAM_CAM _BYTE_ORDER² | GDMA Order³,⁴ | Data |
|----------------|------------------------|--------------------------|---------------------------|---------------|------|
| {BO}{B1}{B2}{B3} | 0                      | 0                        | 0                         | BO,B1,B2,B3   |      |
|                |                        | 1                        | 0                         | BO',B1',B2',B3' |      |
|                |                        |                          | 0                         | BO,B1,B2,B3   |      |
| {B1,BO}{B3,B2} | 1                      | 0                        | 1                         | B1,BO,B3,B2   |      |
|                |                        | 1                        | 0                         | BO',B1',B2',B3' |      |
|                |                        |                          | 1                         | B1',BO',B3',B2' |      |

¹ In RX data, the bits in {} are in big-endian, and are in parallel with each other, while the data in {} is in serial with the data in other {}. Data is received from left to right. Take {BO}{B1}{B2}{B3} as an example. The bits in {BO} are in parallel with each other, but are in serial with the bits in {B1}{B2}{B3}. {BO} is received first.
² Only the configuration listed in the table is valid. Other configurations may cause unexpected data errors.
³ BO ~ B3 represent the bytes of the data to GDMA, from low address to high address.
⁴ In the data to GDMA, Bn'[7:0] = Bn[0:7] (n = 0,1,2,3).

Note:
If only one byte is received each time, CAM_Data_in[7:0] is valid data. For such case, users must connect CAM_Data_in[7:0] with the master.

38.3.6 YUV-RGB Data Format Conversion

LCD_CAM is capable of converting data formats between YUV and RGB. The LCD module and Camera module each have a data format converter. The converters support format conversion:

• under BT601 and BT709 standards
• from RGB565 to YUV422/420/411 (full/limited range)
• from YUV422/YUV411 (full/limited range) to RGB565
• between YUV422/411 (full/limited range) formats

The converter in the LCD module also supports conversion:

• from YUV422/411 (full/limited range) to RGB888 (full/limited range)
• from RGB565 to YUV444 (full/limited range)
• between RGB888 (full/limited range) and RGB565
• from YUV422/411 (full/limited range) to YUV444 (full/limited range)

38.3.6.1 YUV Formats

In LCD_CAM module, assume that there are 8 pixels to be transmitted, corresponding to YUV data [Yᵢ, Uᵢ, Vᵢ] (i = 1 ~ 8). Then:
```