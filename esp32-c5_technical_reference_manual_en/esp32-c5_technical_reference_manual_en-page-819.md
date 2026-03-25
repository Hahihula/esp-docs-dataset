

```markdown
Chapter 20 Debug Assistant

The Debug Assistant module first writes the DMA recorded data to the internal buffer B, and then fetches the data from the buffer and writes it to the configured memory space. When the monitored behaviors are triggered continuously, the generated recording packets may fill the buffer, preventing it from accepting new packets. In such cases, the module dumps the incoming packets and buffers an DMA LOST packet instead before the buffer reaches full capacity. However, it is only possible to know the bus type of the dumped packets when the DMA LOST packet was generated, but not the number of the dumped packets before the generation.

When bus access logging is finished, the recorded data can be read from memory for decoding. The recorded data is in two packet formats, namely, DMA_O packet (corresponding to DMA_O Data bus) and DMA LOST packet. The packet formats are shown in Table 20.5-6 and 20.5-7.

Table 20.5-6. DMA_O Packet Format

| Bit[31:7] | Bit[6:2] | Bit[1] | Bit[0] |
|-----------|----------|--------|--------|
| addr_offset | dma_source | format | anchored(0) |

Table 20.5-7. DMA LOST Packet Format

| Bit[31:3] | Bit[2] | Bit[1] | Bit[0] |
|-----------|--------|--------|--------|
| reserved | lost_source | format | anchored(0) |

The data packet formats show that the DMA_O and DMA LOST packets both have 32 bits. These packets contain the following fields:

*   `format` – the packet type:
    -   0: DMA_O packet
    -   1: DMA LOST packet

*   `addr_offset0` – the address offset of a write operation. Actual address = addr_offset + {MEM_MONITOR_LOG_MIN_REG[31:2], 2'b0}.

*   `dma_source` – the source of DMA access. Details can be found in Table 20.5-5.

*   `lost_source` – the dumped packets when the DMA LOST packet was generated:
    -   0: DMA_O packets were not dumped
    -   1: DMA_O packets were dumped

*   `anchored` – the location of the 32 bits in the data packet:
    -   0: Lower 32 bits
    -   1: Higher 32 bits

The internal buffer of the module is 32 bits wide. When the bus access logging of DMA_O channel groups is enabled and the record data is generated, the DMA_O data packets are buffered. The Debug Assistant module will automatically fetch the buffered data and store it in 32-bit data width into the specified memory space.

The process of packet parsing is described below.

*   Read MEM_MONITOR_LOG_MEM_FULL_FLAG to determine whether there is a data overflow.
```