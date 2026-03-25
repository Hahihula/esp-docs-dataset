

```markdown
|Bit[63:33]|Bit[32]|Bit[31:3]|Bit[2:1]|Bit[0]|
|:-----------|:---------|:----------|:---------|:-------------|
|pc_offset|anchored(1)|addr_offset|format|anchored(0)|
```

```markdown
|Bit[31:8]|Bit[7:3]|Bit[2:1]|Bit[0]|
|:---------------|:------------|:----------|:-----------------|
|addr_offset|dma_source|format|anchored(0)|
```

```markdown
|Bit[31:7]|Bit[6:3]|Bit[2:1]|Bit[0]|
|:-----------|:-------------|:---------|:-----------------|
|reserved|lost_source|format|anchored(0)|
```
```markdown
The data packet formats show that the HP CPU packet is 64 bits, while the other packets are 32 bits each.
These packets have the following fields:

*   `format` – indicates the source of the packet type:
    -   0: HP CPU packet
    -   1: DMA packet
```