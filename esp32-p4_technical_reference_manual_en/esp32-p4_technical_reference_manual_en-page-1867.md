

```markdown
# 39.9 Registers

The addresses in this section are relative to H264 Encoder base address and H264 DMA base address. These base addresses are provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## 39.9.1 H264 Encoder Registers

Register 39.1. H264_SYS_CTRL_REG (0x0000)

| Bit | Description |
|-----|-------------|
| 3   | H264_SYS_RST_PULSE |
| 2   | H264_FRAME_MODE |
| 1   | H264_DMA_MOVE_START |
| 0   | H264_FRAME_START |

- **H264_FRAME_START**: Configures whether to start encoding of a picture.
  - O: Invalid
  - 1: Start encoding of a picture (WT)

- **H264_DMA_MOVE_START**: Configures whether to start moving reference data from external mem.
  - O: Invalid
  - 1: H264 start moving two MB lines of reference frame from external mem to internal mem (WT)

- **H264_FRAME_MODE**: Configures H264 running mode. When field H264_DUAL_STREAM_MODE is set to 1, this field must be set to 1 too.
  - O: GOP mode. Before the start of every GOP, the H264_DMA needs to be reconfigured
  - 1: Frame mode. Before the start of every frame, the H264_DMA needs to be reconfigured (R/W)

- **H264_SYS_RST_PULSE**: Configures whether to reset H264 encoder.
  - O: Invalid
  - 1: Reset H264 encoder (WT)
```