

```markdown
Chapter 6 2D-DMA Controller (2D-DMA)

GoBack

For data transmission, the 2D-DMA generates two types of EOF interrupts:

*   DMA2D_OUT_EOF_CHn_INT, generated when the eof bit of any descriptor in the linked list is set, and the data corresponding to this descriptor has been transmitted. Usually, the eof bit is set in the last descriptor for the transmission of an image. This interrupt is enabled by setting the `DMA2D_OUT_EOF_CHn_INT_ENA` bit.
*   DMA2D_OUT_TOTAL_EOF_CHn_INT, generated when the eof bit of the last descriptor in the linked list is set, and the data corresponding to the last descriptor has been transmitted. This interrupt is enabled by setting the `DMA2D_OUT_TOTAL_EOF_CHn_INT_ENA` bit.

For data reception, the 2D-DMA also generates two types of EOF interrupts:

*   DMA2D_IN_SUC_EOF_CHn_INT, generated when an image has been received. This interrupt is enabled by setting the `DMA2D_IN_SUC_EOF_CHn_INT_ENA` bit.
*   (JPEG only) DMA2D_IN_ERR_CHn_EOF_INT, generated when an image has been received with errors. This interrupt is enabled by setting the `DMA2D_IN_ERR_EOF_CHn_INT_ENA` bit, and is valid only when the channel is connected to JPEG.

When detecting an `DMA2D_OUT_TOTAL_EOF_CHn_INT` or `DMA2D_IN_SUC_EOF_CHn_INT` interrupt, software can read the value of the `DMA2D_OUT_EOF_DES_ADDR_CHn` or `DMA2D_IN_SUC_EOF_DES_ADDR_CHn` field, which stores the address of the finished descriptor. Therefore, the software can tell which descriptors have been used and reclaim them as needed. In RX direction, the address of the descriptor can also be stored to the `DMA2D_IN_ERR_EOF_DES_ADDR_CHn` field when an `DMA2D_IN_ERR_EOF_CHn_INT` interrupt is triggered.

6.4.11 Accessing Memory

Any transmit and receive channels of the 2D-DMA can access the internal memory address space configured by `DMA2D_ACCESS_INTR_MEM_START_ADDR` and `DMA2D_ACCESS_INTR_MEM_END_ADDR`, and the external memory address space configured by `DMA2D_ACCESS_EXTR_MEM_START_ADDR` and `DMA2D_ACCESS_EXTR_MEM_END_ADDR`.

The 2D-DMA can send data in the internal memory in burst mode via the AXI bus. Burst transfer on the AXI bus is enabled by default, and cannot be disabled. Users can configure the number of data bytes in a single AXI burst (burst length) to 8, 16, 32, 64, or 128 bytes via `DMA2D_IN_MEM_BURST_LENGTH_CHn` and `DMA2D_OUT_MEM_BURST_LENGTH_CHn`.

When the 2D-DMA accesses the encrypted external memory space (see Chapter 32 External Memory Encryption and Decryption (XTS_AES)), buffer address pointer and corresponding data should be 16-byte aligned; when it accesses the configured internal memory and non-encrypted external memory space, there are no requirements for descriptor field alignment.

6.4.12 Arbitration

To ensure timely response to peripherals running at a high speed with low latency, the 2D-DMA controller implements two arbitration schemes, based on channel priority and channel weight respectively.

*   Priority arbitration: Each channel can be assigned a priority from 0 ~15 (in total 16 levels). The larger the number, the higher the priority. When several channels perform data transfers at the same time, the
```