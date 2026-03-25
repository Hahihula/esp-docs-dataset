
```markdown
- AHB_DMA_OUT_TOTAL_EOF_CHn_INT, generated when the suc_eof bit of the last descriptor in the linked list is set, and the data corresponding to the last descriptor has been transmitted. This interrupt is enabled by setting the AHB_DMA_OUT_TOTAL_EOF_CHn_INT_ENA bit.

For data reception, the GDMA generates one type of EOF interrupts:

- AHB_DMA_IN_SUC_EOF_CHn_INT, generated when a data segment with an EOF flag has been received. This interrupt is enabled by setting the AHB_DMA_IN_SUC_EOF_CHn_INT_ENA bit.

When detecting an AHB_DMA_OUT_TOTAL_EOF_CHn_INT or AHB_DMA_IN_SUC_EOF_CHn_INT interrupt, software can read the value of the AHB_DMA_OUT_EOF_DES_ADDR_CHn or AHB_DMA_IN_SUC_EOF_DES_ADDR_CHn field, which stores the address of the finished descriptor. Therefore, the software can tell which descriptors have been used and reclaim them as needed.

### 3.4.7 Accessing Memory

Any transmit and receive channels of GDMA can access the memory address space configured by AHB_DMA_ACCESS_INTR_MEM_START_ADDR and AHB_DMA_ACCESS_INTR_MEM_END_ADDR.

To improve data transfer efficiency, GDMA can send data in burst mode. Burst mode is disabled by default, and the burst length can be configured to SINGLE, INCR4, or INCR8 respectively by setting AHB_DMA_IN_DATA_BURST_MODE_SEL_CHn and AHB_DMA_OUT_DATA_BURST_MODE_SEL_CHn to 0, 1, or 2.

When GDMA accesses the configured memory space, there are no requirements for descriptor field alignment.

### 3.4.8 Arbitration

To ensure timely response to peripherals running at a high speed with low latency (such as general-purpose SPI), the GDMA controller implements two arbitration schemes, based on channel priority and channel weight respectively.

- Priority arbitration: Each channel can be assigned a priority from 0 ~ 5 (in total 6 levels). The larger the number, the higher the priority. When several channels perform data transfers at the same time, the GDMA would respond to the transfer requests according to priority levels, and the channel with higher priority would get a response more timely.

- Weight arbitration:

    - Each channel is assigned a weight (i.e., the number of tokens) from 0 ~ 15. The GDMA divides the AHB bus clock period into multiple time slots, and in each time slot, the number of transfers performed by a channel is determined by the number of its tokens. Every time a channel performs a data transfer, one of its tokens is spent. If all of its tokens have been spent in a time slot, then this channel's transfer request will no longer be responded to until the time slot expires, or until tokens of all channels have been spent and the new time slot starts.

    - If the number of tokens assigned to a channel is not zero, the GDMA waits for this channel's tokens to be spent even if it does not have data transfer requests, and will not exit from this time slot ahead of expiration. This leads to a waste of bandwidth. Therefore, the GDMA provides weight arbitration optimization. When this feature is enabled, a channel without data transfer requests will not be involved in the arbitration and its tokens will be ignored. When all channels no longer have transfer
```