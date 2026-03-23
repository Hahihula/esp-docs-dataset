

```markdown
- In loop mode, writing to specified address space is performed in loops. When writing reaches the end address, it will return to the starting address and continue, overwriting the previously recorded data.
  For example, 10 writes (1 ~ 10) write to address space 0 ~ 4. After the 5th write writes to address 4, the 6th write will start writing from address 0. The 6th to 10th writes will overwrite the previous data written by 0 ~ 4 writes.

- In non-loop mode, when writing reaches the end address, it will stop at the end address, not overwriting the previously recorded data.
  For example, 10 writes (1 ~ 10) write to address space 0 ~ 4. After the 5th write writes to address 4, the 6th to 10th writes will write at address 4. Only the data written by the last (10th) write will be retained at address 4.

6. Configure bus enable registers.

- Enable CPU or DMA bus access logging with ASSIST_DEBUG_LOG_ENA. CPU and DMA bus access logging can be enabled at the same time.

When bus access logging is finished, the recorded data can be read from memory for decoding. The recorded data is in two packet formats, namely CPU packet (corresponding to CPU bus) and DMA packet (corresponding to DMA bus). The packet formats are shown in Table 17.4-1 and 17.4-2:

Table 17.4-1. CPU Packet Format

| Bit[49:29] | Bit[28:2] | Bit[1:0] |
|------------|-----------|----------|
| addr_offset | pc_offset | format   |

Table 17.4-2. DMA Packet Format

| Bit[24:6] | Bit[5:2] | Bit[1:0] |
|-----------|----------|----------|
| addr_offset | dma_source | format   |

It can be seen from the data packet formats that the CPU packet size is 50 bits and DMA packet size 25 bits. The packet formats contain the following fields:

- format – the packet type. 1: CPU packet; 3: DMA packet; other values: reserved.
- pc_offset – the offset of the PC register at time of access. Actual PC = pc_offset + 0x4000_0000.
- addr_offset – the address offset of a write operation. Actual address = addr_offset + ASSIST_DEBUG_LOG_MIN_REG.
- dma_source – the source of DMA access. Refer to Table 17.4-3.

Table 17.4-3. DMA Source

| Value | Source |
|-------|--------|
| 1     | SPI2   |
| 2     | reserved |
| 3     | reserved |
| 4     | AES    |
```