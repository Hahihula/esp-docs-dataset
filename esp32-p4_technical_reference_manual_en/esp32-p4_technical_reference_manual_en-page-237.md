

```markdown
## 4.4.8 Accessing Memory

The transmit and receive channels of GDMA-AHB can access the internal and external memory space configured by AHB_DMA_ACCESS_INTR_MEM_START_ADDR and AHB_DMA_ACCESS_INTR_MEM_END_ADDR.

The transmit and receive channels of GDMA-AXI can access:

* Internal memory space configured by AXI_DMA_ACCESS_INTR_MEM_START_ADDR and AXI_DMA_ACCESS_INTR_MEM_END_ADDR.
* External memory space configured by AXI_DMA_ACCESS_EXTR_MEM_START_ADDR and AXI_DMA_ACCESS_EXTR_MEM_END_ADDR.

To improve data transfer efficiency, GDMA can send data in burst mode. For GDMA-AHB, this mode is disabled by default, and can be enabled for receive channels by setting AHB_DMA_IN_DATA_BURST_EN_ChN, and enabled for transmit channels by setting AHB_DMA_OUT_DATA_BURST_EN_ChN. For GDMA-AXI, this mode is enabled by default, and cannot be disabled. Users can configure the number of data bytes in a single AXI burst (burst length) to 8, 16, 32, 64, or 128 bytes via AXI_DMA_IN_BURST_SIZE_SEL_ChN and AXI_DMA_OUT_BURST_SIZE_SEL_ChN.

When GDMA-AHB and GDMA-AXI access the configured internal memory and non-encrypted external memory space, there are no requirements for descriptor field alignment; when they access the encrypted external memory space (see Chapter 32 External Memory Encryption and Decryption (XTS_AES)), buffer address pointer and data should be 16-byte aligned, and other fields are not required to be aligned.

## 4.4.9 Arbitration

To ensure timely response to peripherals running at a high speed with low latency (such as SPI), the GDMA controller implements two arbitration schemes, based on channel priority and channel weight respectively.

* Priority arbitration: Each channel can be assigned a priority from 0 ~ 5 (in total 6 levels). The larger the number, the higher the priority. When several channels perform data transfers at the same time, the GDMA would respond to the transfer requests according to priority levels, and the channel with higher priority would get a response more timely.
* Weight arbitration:

    - Each channel is assigned a weight (i.e., the number of tokens) from 0 ~ 15. The GDMA divides the AHB or AXI bus clock period into multiple time slots, and in each time slot, the number of transfers performed by a channel is determined by the number of its tokens. Every time a channel performs a data transfer, one of its tokens is spent. If all of its tokens have been spent in a time slot, then this channel's transfer request will no longer be responded to until the time slot expires, or until tokens of all channels have been spent and the new time slot starts.
    - If the number of tokens assigned to a channel is not zero, the GDMA waits for this channel's tokens to be spent even if it does not have data transfer requests, and will not exit from this time slot ahead of expiration. This leads to a waste of bandwidth. Therefore, the GDMA provides weight arbitration optimization. When this feature is enabled, a channel without data transfer requests will not be involved in the arbitration and its tokens will be ignored. When all channels no longer have transfer
```