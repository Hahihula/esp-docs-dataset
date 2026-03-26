

```markdown
Register 35.1. JPEG_CONFIG_REG (0x0000)

Continued from the previous page...

JPEG_DECODETIMEOUT_TASK_SEL Configures the reset mode upon the decoder timeout.
    0: Software uses reset to abort the decoding process
    1: Hardware automatically aborts decoding process
        (R/W)

JPEG_SOFT_RST Configures whether or not to apply soft reset to the JPEG Codec.
    0: Release the soft reset
    1: Apply soft reset to the JPEG Codec (the register configuration value will not be reset)
        (R/W)

JPEG_FIFO_RST Configures whether or not to apply FIFO reset to the JPEG Codec.
    0: Release the FIFO reset
    1: Apply FIFO reset to the JPEG Codec
        (R/W)

JPEG_PIXEL_REV Configures whether or not to reverse the original image's pixel order.
    0: Not reverse
    1: Reverse
        (R/W)

JPEG_TAILER_EN Configures whether or not to add EOI marker "0xFFD9" at the end of bitstream.
    0: Not add
    1: Add
        (R/W)

JPEG_PAUSE_EN Configures whether or not to pause the JPEG Codec.
    0: Not pause
    1: Pause
        (R/W)

JPEG_MODE Configures if the JPEG Codec is working as an encoder or a decoder.
    0: Encoder
    1: Decoder
        (R/W)
```