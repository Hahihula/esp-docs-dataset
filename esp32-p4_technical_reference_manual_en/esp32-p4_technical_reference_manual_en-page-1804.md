
```markdown
| GDMA Data Order¹ | LCD_CAM_LCD _BYTE_MODE | LCD_CAM_LCD _BIT_ORDER | LCD_CAM_LCD _BYTE_ORDER² | Output Data Order³,⁴ |
|------------------|------------------------|-------------------------|----------------------------|-----------------------|
|                  | 0                      | 0                       | 0                          | {BO}{B1}{B2}{B3}{B4}{B5} |
|                  |                        | 1                       | 0                          | {BO}'{B1}'{B2}'{B3}'{B4}'{B5}' |
|                  | 1                      | 0                       | 0                          | {B1,BO}{B3,B2}{B5,B4}   |
|                  |                        |                         | 1                          | {BO,B1}{B2,B3}{B4,B5}   |
|                  | BO,B1,B2,B3,B4,B5     | 1                       | 0                          | {B1',BO}'{B3',B2}'{B5',B4}' |
|                  |                        |                         | 1                          | {BO',B1}'{B2',B3}'{B4',B5}' |
|                  |                        | 0                       | 0                          | {B2,B1,BO}{B5,B4,B3}    |
|                  | 2                      |                         | 1                          | {BO,B1,B2}{B3,B4,B5}    |
|                  |                        | 1                       | 0                          | {B2',B1',BO}'{B5',B4',B3}' |
|                  |                        |                         | 1                          | {BO',B1',B2}'{B3',B4',B5}' |
```

¹ BO ~ B5 represent the bytes of the data from GDMA, from low address to high address.  
² Only the configuration listed in the table is valid. Other configurations may cause unexpected data errors.  
³ In output data, the bits in {} are in big-endian, and are in parallel with each other, while the data of {} is in serial with the data of {}. Data is sent out from left to right. Take {BO}{B1}{B2}{B3} as an example. The bits in {BO} are in parallel with each other, but are in serial with the bits in {B1}{B2}{B3}. {BO} is sent out first.  
⁴ In output data, Bn'[7:0] = Bn[0:7] (n = 0,1,2,3,4,5).

Stage Two: Data Color Space Conversion
At this stage, the data undergoes color space conversion. For detailed configurations, please refer to Section 38.3.6.

Note:
Users can skip Stage Two by configuring LCD_CAM_LCD_CONV_ENABLE as 0, in which case the output of Stage One will directly become the input of Stage Three.

Stage Three: Data Post-processing
At this stage, configure the following registers to adjust the bit and byte order of the output data.

*   `LCD_CAM_LCD_WIRE_MODE`
    -  0: The bit width of the data transmitted to GPIO is 8 bits.
    -  1: The bit width of the data transmitted to GPIO 16 bits.
    -  2: The bit width of the data transmitted to GPIO is 24 bits.

*   `LCD_CAM_LCD_DOUT_BIT_ORDER`
    -  0: Do not invert.
    -  1: Invert the output data bit order.

*   `LCD_CAM_LCD_DOUT_BYTE_SWIZZLE_ENABLE`
    -  0: Disable LCD output data byte reordering.
    -  1: Enable LCD output data byte reordering by configuring LCD_CAM_LCD_DOUT_BYTE_SWIZZLE_MODE. For the reordering results see Table 38.3-3.
```