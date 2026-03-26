

```markdown
## 35.9 Registers

The addresses in this section are relative to the JPEG Codec base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 35.1. JPEG_CONFIG_REG (0x0000)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 32 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|---|---|---|---|---|---|---|---|----|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|     | 0  | 00 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |    |   0 | 1 | 0 | O | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 1 | 1 | 1 | 0 | 0 | 0 |
|     | Reset |

JPEG_FSM_RST Configures whether or not to reset the state machine of JPEG Codec.
O: Invalid. No effect
1: Reset the state machine (WT)

JPEG_JPEG_START Configures whether or not to start compressing a new image.
O: Invalid. No effect
1: Start compressing a new image (WT)

JPEG_QNR_PRECISION Configures the quantization coefficient table precision for the encoder.
O: 8-bit precision
1: 16-bit precision (R/W)

JPEG_FF_CHECK_EN Configures whether or not to add "0x00" after "0xFF".
O: Not add
1: Add (R/W)

JPEG_SAMPLE_SEL Configures the format of the image to be compressed.
O: YUV444
1: YUV422
2: YUV420
3: Invalid. No effect (R/W)
```