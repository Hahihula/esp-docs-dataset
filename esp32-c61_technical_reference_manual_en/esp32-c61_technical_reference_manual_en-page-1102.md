

```markdown
| S | D | Command Index 110100b | R/W flag | Function Number | RAW flag | Stuff | Register Address | Stuff of Stuff Bits | CRC7 | E |
|----:|:---|:-----------------------|:---------|:-----------------|:----------|:-------|:------------------|:--------------------|:-----|:|
| 1 |   |                      6 |    1     |        3         |    1      |   17   |       1           |          8          |   7  | 1 |
```

**Figure 30.5-1. CMD52 Content**

IO_RW_EXTENDED (CMD53) initiates the transfer of packets of an arbitrary length. Figure 30.5-2 shows its fields. For details on each field, please refer to the SDIO Specification V2.00.

```markdown
| S | D | Command Index 110101b | R/W flag | Function Number | Block Mode 1b | OP Code | Register Address | Byte/Block Count Roundup (Packet_length/Block_Size) | CRC7 | E |
|----:|:---|:-----------------------|:---------|:-----------------|:--------------|:--------|:------------------|:-----------------------------------------------------|:-----|:|
| 1 |   |                      6 |    1     |        3         |      1        |    17   |                   |                                                        |   7  | 1 |
```

**Figure 30.5-2. CMD53 Content**

### 30.5.3 I/O Function 0 Address Space

I/O function 0 is used only for Card Common Control Registers (CCCR), Function Basic Registers (FBR), and Card Information Structure (CIS) operations. Figure 30.5-3 shows its address space map, as specified by the SDIO Specification. For details on each section in this map, please refer to the SDIO Specification V2.00.
```