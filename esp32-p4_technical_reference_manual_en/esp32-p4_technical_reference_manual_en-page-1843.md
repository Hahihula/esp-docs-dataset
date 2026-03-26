

```markdown
- out_fifo: This module receives the data returned by the AXI read request and waits for h264 to read, or RX channel 5 to read. TX channel 0/1/2 is for h264 to read, and TX channel 3/4 is for RX channel 5 to read.
- arb: This module receives read/write requests for external or internal memory, and arbitrates the read/write requests. The requests are sent to the rdcmd_fifo and wrcmd_fifo modules of external memory, and the rdcmd_fifo and wrcmd_fifo modules of internal memory respectively.
- wrcmd_fifo: This module catches the AXI write request arbitrated by the arb module, and cuts the write request and data into multiple 8-byte data chunks before sending them to the async_in_fifo module.
- rdcmd_fifo: This module catches the AXI read request arbitrated by the arb module and sends the read request to the async_in_fifo module.
- bak_fifo: This module caches the read/write request information arbitrated by the arb module, including channel id, AXI_id, read/write request data length, read/write request source and read request starting address. The module finds the information corresponding to the request based on the AXI_id returned by the async_out_fifo module, and sends the completion information of the request and the read data in the async_out_fifo module to the corresponding channel.
- async_in_fifo: This module is used to receive AXI requests from the wrcmd_fifo module and rdcmd_fifo module, and synchronize the request from H264_DMA core clock domain to the AXI clock domain, waiting for the AXI master to read.
- async_out_fifo: This module is used to receive the read data returned by the AXI_master_inter/AXI_master_extern module and the completion of the read/write request, and synchronize it from the AXI clock domain to the H264_DMA core clock domain.
- AXI_master_inter/AXI_master_extern: This module reads the read/write request in the async_in_fifo module and converts it into an AXI bus protocol format output. The module receives the read data and read/write completion returned by the AXI slave and converts it into an internal private interface. The resulting format is written to the async_out_fifo module. The AXI_master_inter module is used to access the internal memory space, and the AXI_master_extern module is used to access the external memory space.
```

### 39.5.2.2 Linked List Descriptor

H264_DMA linked list descriptor is shown in the figure 39.5-3:
```markdown
Espressif Systems
1843
ESP32-P4 TRM
PRELIMINARY
Submit Documentation Feedback
```