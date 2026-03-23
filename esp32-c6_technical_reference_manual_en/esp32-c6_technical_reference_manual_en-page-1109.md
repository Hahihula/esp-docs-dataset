

```markdown
| S | D | Command Index 110100b | R/W flag | Function Number | RAW flag | Stuff | Register Address | RAW flag | Write Data or Stuff Bits | CRC7 E |
|---|---|------------------------|----------|-----------------|----------|-------|------------------|----------|---------------------------|--------|
| 1 | 1 | 6                     | 1        | 3               | 1        | 1     | 17               | 1        | 8                         | 7      | 1 |
```

Figure 34.5-1. CMD52 Content

```markdown
| S | D | Command Index 110101b | R/W flag | Function Number | Block Mode 1b | OP Code | Register Address | Byte/Block Count Roundup (Packet length/Block size) | CRC7 E |
|---|---|------------------------|----------|-----------------|---------------|---------|------------------|----------------------------------------------------|--------|
| 1 | 1 | 6                     | 1        | 3               | 1             | 17      |                  |                                                    |        |
```

Figure 34.5-2. CMD53 Content

### 34.5.3 I/O Function 0 Address Space

I/O function 0 is only used for Card Common Control Registers (CCCR), Function Basic Registers (FBR), and Card Information Structure (CIS) operations. Figure 34.5-3 shows its address space map, which is specified by the SDIO Specification. For what each section in this map means, please refer to the Specification.

```markdown
| 0x000000-0x0000FF | CCCR |
|---|------|
| 0x000100-0x0001FF | FBR (Function 1) |
| 0x000200-0x0002FF | FBR (Function 2) |
| 0x000300-0x0003FF | FBR (Function 3) |
| 0x000700-0x0007FF | FBR (Function 7) |
| 0x000800-0x000FFF | RFU |
| 0x001000-0x017FFF | CIS Area (common and per-function) |
| 0x018000-0x01FFFF | RFU |
```

Figure 34.5-3. Function 0 Address Space

As defined in the SDIO Specification, CCCR are common control registers, FBR are control configuration registers for each function, and CIS are status registers for storing card information, such as version, power
```