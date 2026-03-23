

```markdown
|Bit[31:9]|Bit[8:4]|Bit[3:2]|Bit[1:0]|
|---------:|--------:|--------:|--------:|
|addr_offset|dma_source|format|anchored(1)|
```

**Table 18.4-4. LOST Packet Format**

```markdown
|Bit[31:4]|Bit[3:2]|Bit[1:0]|
|---------:|--------:|--------:|
|reserved|format|anchored(1)|
```

It can be seen from the data packet formats that the HP CPU packet size is 64 bits, LP CPU packet 32 bits, DMA packet size 32 bits, and LOST packet 32 bits. These packets contain the following fields:

*   `format` – the packet type. O: HP CPU packet; 1: DMA packet; 2: LP CPU packet; 3: LOST packet.
*   `pc_offset` - the offset of the PC register at the time of access. Actual PC = pc_offset + 0x4000_0000.
*   `addr_offset` - the address offset of a write operation. Actual address = addr_offset + MEM_MONITOR_LOG_MIN_REG.
*   `dma_source` - the source of DMA access. Refer to Table 18.4-5. For more information on the values 16 ~ 31 in the table, please refer to 4 GDMA Controller (GDMA).
*   `anchored` - the location of the 32 bits in the data packet. 1 indicates the lower 32 bits. 2 indicates the higher 32 bits.

**Table 18.4-5. DMA Access Source**

```markdown
|Value|Source|
|-----:|------|
|0     |HP CPU|
|1     |LP CPU|
|2     |reserved|
|3     |SDIO_SLV|
|4     |reserved|
|5     |MEM_MONITOR|
|6     |TRACE|
|7 ~ 15|reserved|
||See the peripherals corresponding to the values 0 ~ 15 in Chapter 4 GDMA Controller (GDMA) > Table 4.4-1 Selecting Peripherals via Register Configuration. For example, the source corresponding to the value 16 is the peripheral corresponding to the value 0 in that table, the source corresponding to 17 is the peripheral corresponding to 1 in that table, and etc.|
|16 ~ 31||
```

The internal buffer of the module is 32 bits wide. When the HP CPU, LP CPU, or DMA bus access logging are all enabled at the same time and the record data is generated at the same time, the DMA data packets are first buffered, then the HP CPU packets, and finally the LP CPU packets. This priority of buffering packets also applies to the case where only two types of packets are generated at the same time. The Debug Assistant will automatically fetch the buffered data and store it in 32-bit data width into the specified memory space.
```