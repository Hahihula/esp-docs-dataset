

```markdown
- JPEG_MARKER_ERR_OTHER_SCAN_INT: Triggered when there is an error in the non-first scan header information parsed by the decoder. The error type is the same as the errors that trigger JPEG_MARKER_ERR_FST_SCAN_INT.
- JPEG_UNDET_INT: Triggered when the bitstream of an image is completely read from 2D DMA but the SOS marker is not read.
- JPEG_DECODE_TIMEOUT_INT: Triggered when the decoder is timeout. Section 35.7.2 describes how this interrupt will occur.

The above interrupt sources can only be triggered when the interrupt enable register `interrupt_source_name_ENA` is set to 1. Write 1 to `interrupt_source_name_CLR` will clear the interrupt.

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.
```

## 35.7 Programming Procedures

### 35.7.1 JPEG Encoder

When the JPEG codec is working as an encoder, the configuration process is:

1. Activate the JPEG codec:
   - Set `HP_SYS_CLKRST_JPEG_SYS_CLK_EN` to 1 to enable the JPEG codec clock;
   - Set `HP_SYS_CLKRST_RST_EN_JPEG` to 0 to release the JPEG codec system level reset.

2. Configure the JPEG codec:
   - Set `JPEG_SOFT_RST` to 1 to reset the JPEG codec, and then set `JPEG_SOFT_RST` to 0 to release the JPEG codec reset.
   - Set `JPEG_MODE` to 0 to configure the JPEG codec to be used as an encoder.
   - Select the original image format by configuring the following registers:
     - Format:
       * `JPEG_COLOR_SPACE`
       * `JPEG_EXTD_COLOR_SPACE_EN`
       * `JPEG_EXTD_COLOR_SPACE`
     - Pixel order: `JPEG_PIXEL_REV`
       See details in Table 35.5-1.
   - Select whether to add the EOI marker (0xFFD9) at the end of the bitstream by configuring `JPEG_TAILER_EN`.
```