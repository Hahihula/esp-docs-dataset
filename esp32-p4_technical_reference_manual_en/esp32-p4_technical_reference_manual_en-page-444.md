

```markdown
Chapter 6 2D-DMA Controller (2D-DMA)

Register 6.24. DMA2D_IN_SCRAMBLE_CHO_REG (0x0550)

| Bit | Field Name                        | Description                                                                 |
|-----|------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                    |                                                                             |
|     |                                    | Reset                                                                       |
|     |                                    | 6   5   3   2   0                                                            |
|     |                                    | 0x0                     0x0                                                    |

DMA2D_IN_SCRAMBLE_SEL_PRE_CHO Configures the byte order scrambling before the color space conversion for RX channel 0.
0: BYTE2-1-O
1: BYTE2-O-1
2: BYTE1-O-2
3: BYTE1-2-O
4: BYTEO-2-1
5: BYTEO-1-2
Others: Invalid
(R/W)

DMA2D_IN_SCRAMBLE_SEL_POST_CHO Configures the byte order scrambling after the color space conversion for RX channel 0.
0: BYTE2-1-O
1: BYTE2-O-1
2: BYTE1-O-2
3: BYTE1-2-O
4: BYTEO-2-1
5: BYTEO-1-2
Others: Invalid
(R/W)
```