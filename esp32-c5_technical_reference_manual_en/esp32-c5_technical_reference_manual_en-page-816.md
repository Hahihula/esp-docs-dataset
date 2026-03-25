

```markdown
| Bit[31:7] | Bit[6:3]   | Bit[2:1] | Bit[0]     |
|-----------|------------|----------|------------|
| reserved  | lost_source| format   | anchored(0)|
```

The data packet formats show that the HP CPU packet has 64 bits, and other packets have 32 bits each. These packets have the following fields:

* **format** – the packet type:
    - 0: HP CPU packet
    - 1: DMA packet
    - 2: LP CPU packet
    - 3: LOST packet

* **pc_offset** – the offset of the HP CPU PC register at the time of access. Actual PC = pc_offset + 0x0000_0000.

* **addr_offset** – the address offset of a write operation. Actual address = addr_offset + {MEM_MONITOR_LOG_MIN_REG[31:2], 2'b0}.

* **dma_source** – the source of DMA access. Details can be found in Table 20.5-5, where sources corresponding to value 16 ~ 31 are detailed in 5 GDMA Controller (GDMA).

* **lost_source** – the dumped packets when the LOST packet was generated.

    - Bit[4:3]:
        * 0: HP CPU packets were not dumped
        * 3: HP CPU packets were dumped
        * Other values: reserved

    - Bit[5]:
        * 0: DMA packets were not dumped
        * 1: DMA packets were dumped

    - Bit[6]:
        * 0: LP CPU packets were not dumped
        * 1: LP CPU packets were dumped

* **anchored** – the location of the 32 bits in the data packet:
    - 0: Lower 32 bits
    - 1: Higher 32 bits

Table 20.5-5. DMA Access Source

| Value | Source   |
|-------|----------|
| 0     | HP CPU   |
| 1     | LP CPU   |
```