

```markdown
| Bit[31:3] | Bit[2]   | Bit[1] | Bit[0] |
|-----------|----------|--------|--------|
| reserved  | lost_source | format | anchored(0) |
```

The data packet formats show that the DMA_O and DMA LOST packets are both 32 bits. These packets contain the following fields:

*   **format** – indicates the source of the packet type:
    -   0: DMA_O packet
    -   1: DMA LOST packet

*   **addr_offset** – indicates the address offset of a write operation. Actual address = addr_offset + {MEM_MONITOR_LOG_MEM_REG[31:2], 2'b0}.

*   **dma_source** – the source of DMA access. Details are in Table 18.5-4.

*   **lost_source** – indicates which packets were discarded when the DMA LOST packet was generated:
    -   0: DMA_O packets were not discarded
    -   1: DMA_O packets were discarded

*   **anchored** – indicates the location of the 32 bits in the data packet:
    -   0: Lower 32 bits
    -   1: Higher 32 bits

The internal buffer of the module is 32 bits wide. When the bus access logging of the DMA_O channel groups is enabled and the record data is generated, the DMA_O data packets are buffered. The Debug Assistant module automatically fetches the buffered data and stores it in 32-bit width in the specified memory space.

The packet parsing process is described below.

*   Read MEM_MONITOR_LOG_MEM_FULL_FLAG to determine whether there is a data overflow.
    -   If no, the address space to read is `MEM_MONITOR_LOG_MEM_START_REG ~ MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG – 4`.
    -   If yes and loop mode is enabled, the address space is
      ```
      MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG ~ MEM_MONITOR_LOG_MEM_END_REG and
      MEM_MONITOR_LOG_MEM_START_REG ~ MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG – 4.
      ```
    -   If yes and loop mode is not enabled, the address space is `MEM_MONITOR_LOG_MEM_START_REG ~ MEM_MONITOR_LOG_MEM_END_REG`.

*   Read and parse data from the starting address. Read 32 bits at a time.

After packet parsing is complete, clear the MEM_MONITOR_LOG_MEM_FULL_FLAG bit by setting `MEM_MONITOR_CLR_LOG_MEM_FULL_FLAG` to 1.
```