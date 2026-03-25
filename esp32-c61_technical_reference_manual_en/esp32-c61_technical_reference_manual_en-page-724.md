
```markdown
- 2: Reserved
- 3: LOST packet


* **pc_offset** - indicates the offset of the HP CPU PC register at the time of access. Actual PC = pc_offset + 0x0000_0000.

* **addr_offset** - the address offset of a write operation. Actual address = addr_offset + {MEM_MONITOR_LOG_MIN_REG[31:2], 2'b0}.


* **dma_source** - the source of DMA access. Details can be found in Table 18.5-4, where sources corresponding to values 16 ~ 31 are detailed in 3 GDMA Controller (GDMA).

* **lost_source** - indicates which packets were discarded when the LOST packet was generated.

    - Bit[4:3]:
        * 0: HP CPU packets were not discarded
        * 3: HP CPU packets were discarded
        * Other values: reserved

    - Bit[5]:
        * 0: DMA packets were not discarded
        * 1: DMA packets were discarded

    - Bit[6]: Reserved


* **anchored** - indicates the location of the 32 bits in the data packet:
    - 0: Lower 32 bits
    - 1: Higher 32 bits
```