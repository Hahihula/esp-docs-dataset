

```markdown
- H264_DMA_OUT/IN_MEM_BURST_LENGTH_CHx: This register controls the AXI burst length of the corresponding channel.
  - 0: 8 bytes. 1: 16 bytes. 2: 32 bytes. 3: 64 bytes. 4: 128 bytes.
    - In TX channel, x can be 0 ~ 4. In RX channel, x can be 0 ~ 5.
    - The burst length of TX channel 2 and RX channel 2 must be configured the same.

- H264_DMA_OUT_REORDER_ENCHO: This register controls the TX channel 0 reorder enable. When the linked list descriptor configuration HB is not 16 in TX channel 0, this register must be configured as 1.

- H264_DMA_BLOCK_START_ADDR_CH5: This register controls the data starting address of the RX channel 5. The register configuration must be consistent with the data buffer address in the linked list descriptor of the TX channel 1.

- H264_DMA_BLOCK_ROW_LENGTH_4LINE_CH5: This register specifies the number of bytes contained in a row block of 4 lines. The data size is (NUM_H_MB x (16 x 4 + 8 x 4 x 2)).

- H264_DMA_BLOCK_ROW_LENGTH_12LINE_CH5: This register specifies the number of bytes contained in a row block of 12 lines. The data size is (NUM_H_MB x (16 x 12 + 8 x 4 x 2)).

- H264_DMA_BLOCK_LENGTH_4LINE_CH5: This register specifies the number of bytes contained in a block of 4 lines. The data size is (16 x 4 + 8 x 4 x 2).

- H264_DMA_BLOCK_LENGTH_12LINE_CH5: This register specifies the number of bytes contained in a block of 12 lines. The data size is (16 x 12 + 8 x 4 x 2).
```

## 39.6 Interrupts

ESP32-P4’s H264 Encoder can generate the following interrupt signals, which are then sent to the **Interrupt Matrix**.

- H264_REG_INT
- H264_DMA_IN_CHO_INT
- H264_DMA_IN_CH1_INT
- H264_DMA_IN_CH2_INT
- H264_DMA_IN_CH3_INT
- H264_DMA_IN_CH4_INT
- H264_DMA_IN_CH5_INT
- H264_DMA_OUT_CHO_INT
- H264_DMA_OUT_CH1_INT
- H264_DMA_OUT_CH2_INT
- H264_DMA_OUT_CH3_INT
- H264_DMA_OUT_CH4_INT

There are several internal interrupt sources from H264 Encoder that can generate the above interrupt signals.
```