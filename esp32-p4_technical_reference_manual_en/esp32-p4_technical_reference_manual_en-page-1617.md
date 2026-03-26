

```markdown
Register 35.1. JPEG_CONFIG_REG (0x0000)

Continued from the previous page...

JPEG_DMA_LINKLIST_MODE Represents 2D DMA linked list mode.
O: Invalid. No effect
1: 2D DMA uses linked lists to configure
   (RO)

JPEG_DEBUG_DIRECT_OUT_EN Configures whether or not to enable debug mode for encoder.
O: Disable debug mode, the encoder will work in normal mode
1: Enable debug mode, the input image will be directly output by the encoder
   (R/W)

JPEG_QNR_FIFO_EN Configures whether or not to enable FIFO mode when configuring quantization coefficient tables.
O: Disable. Use non-FIFO mode
1: Enable
   (R/W)

JPEG_LQNR_TBL_SEL Configures the luminance quantization table ID for the encoder. (R/W)

JPEG_CQNR_TBL_SEL Configures the chrominance quantization table ID for the encoder. (R/W)

JPEG_COLOR_SPACE Configures the original image's color space.
O: RGB888
1: YUV422
2: RGB565
3: GRAY
   (R/W)

JPEG_DHT_FIFO_EN Configures whether or not to enable FIFO mode when configuring Huffman tables.
O: Disable. Use non-FIFO mode
1: Enable
Note that to read Huffman tables only non-FIFO mode is supported.
(R/W)

JPEG_MEM_CLK_FORCE_ON Configures whether or not to force on memory's clock gate.
O: Not force on
1: Force on
   (R/W)

JPEG_DECODE_TIMEOUT_THRES Configures decode timeout period to trigger JPEG_DECODE_TIMEOUT_INT_RAW. The clock cycles of timeout period = 2^JPEG_DECODE_TIMEOUT_THRES - 1. (R/W)

Continued on the next page...
```