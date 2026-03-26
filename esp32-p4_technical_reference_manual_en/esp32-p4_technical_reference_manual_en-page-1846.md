

```markdown
## 39.5.2.4 Transfer Reset

In order to ensure the safe reset of H264_DMA and prevent channel from being stuck, the reset of H264_DMA channel must be carried out according to the following procedure:

1. Write 1 to register H264_DMA_OUT/IN_CMD_DISABLE_CHx of the corresponding channel.
2. Wait for H264_DMA_OUT/IN_RESET_AVAIL_CHx of the corresponding channel to be set.
3. Write 1 to register H264_DMA_OUT/IN_RST_CHx of the corresponding channel.
4. Write 0 to register H264_DMA_OUT/IN_RST_CHx of the corresponding channel.

The registers related to channel reset are as follows:

*   **H264_DMA_OUT/IN_CMD_DISABLE_CHx**: This register controls whether the corresponding channel of H264_DMA stops initiating read/write requests to AXI. Setting this register to 1 means that the corresponding channel stops initiating read/write requests to AXI. Setting this register to 0 means that the corresponding channel can initiate read/write requests to AXI, x can be 0, 1, and 2 in TX channel, indicating the registers corresponding to channels 0, 1, and 2. In RX channel, they can be 0, 1, 2, 3, 4, and 5, indicating the registers corresponding to channels 0, 1, 2, 3, 4, and 5.
*   **H264_DMA_OUT/IN_RESET_AVAIL_CHx**: This register indicates whether the channel corresponding to H264_DMA can be safely reset. If this register is 1, it means that the corresponding channel can be safely reset. If this register is 0, it means that the corresponding channel cannot be safely reset.
*   **H264_DMA_OUT/IN_RST_CHx**: This register controls whether the corresponding channel of H264_DMA performs soft reset. Setting this register to 1 means that the corresponding channel performs a soft reset. Setting this register to 0 means that the corresponding channel does not perform a soft reset.

Notes:

*   Since TX channel 3, TX channel 4, and RX channel 5 are bound, these three channels only have one set of H264_DMA_OUT/IN_CMD_DISABLE_CH5, H264_DMA_OUT/IN_RESET_AVAIL_CH5, and H264_DMA_OUT/IN_RST_CH5 registers. When resetting these three channels, you only need to operate this group of registers to realize the safe reset of the three H264_DMA channels.
*   In order to ensure the completion of data transmission, before resetting RX channel 0, RX channel 1, RX channel 3, and RX channel 4, you need to check whether the corresponding channel linked list descriptor is written back successfully. Only after the linked list descriptor of the channel is written back successfully, which means all data transmission of the channel is completed, can the channel be reset. If the MV merging function is not enabled or the number of video frames in a GOP is 1, which means the register H264_GOP_NUM is configured as 1, there is no need to check whether the linked list descriptor of RX channel 3 is written back successfully.

## 39.5.2.5 Channel Configuration

Before the software starts H264_DMA, it needs to configure H264_DMA first. The configuration consists of register configuration and linked list descriptor configuration.

Linked list descriptor configuration: The channels that need to be configured with descriptors are TX channel 0 ~ TX channel 4 and RX channel 0 ~ RX channel 4. The linked list descriptors are all circular linked lists.

1. Configure the channel of reading the original picture (TX channel 0):
```