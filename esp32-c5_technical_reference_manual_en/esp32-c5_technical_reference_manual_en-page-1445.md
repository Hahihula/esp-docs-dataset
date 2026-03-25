

```markdown
| Address | Register Name     | Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|---------|-------------------|-------|-------|-------|-------|-------|-------|-------|-------|
| 0x08    | Card Capability   | O     | O     | R/W   | 1     | O     | 1     | 1     | 1     |
|         |                   | (4BLS)| (LSC) | (E4MI)| (S4MI)| (SBS) | (SRW) | (SMB) | (SDC) |
| 0x09-   | Common CIS        |       |       | Address 0x09: 0x0; Address 0xA0: 0x10; Address 0xB: 0x0 | Pointer to card's common CIS | |
| 0x0B    | Pointer           |       |       |                                                       |                           |     |     |     |     |
| 0x0C    | Bus Suspend       |       | O (RFU) | O (BR) | O (BS) |
| 0x0D    | Function Select   | O (DF)| O (RFU) | O (FS[3:0]) | |
| 0x0E    | Exec Flags        |       | O (EX[7:1]) | O (EXM) | |
| 0x0F    | Ready Flags       |       | O (RF[7:1]) | O (RFM) | |
| 0x10-   | FNO Block Size    |       | R/W (Supported range: 0-512) | I/O block size for Function 0 | |
| 0x11    |                   |       |                               |                           |     |     |     |     |     |
| 0x12    | Power Control     | O (RFU)| R/W (EMPC) | 1 (SMPC) | |
| 0x13    | High-Speed        | O (RFU)| R/W (EHS) | Note a (SHS) | |

a Set SHS using HINF_HIGHSPEED_ENABLE in HINF_CFG_DATA1_REG.

Table 39.5-2. SDIO Slave FBR Configuration
| Address | Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|---------|-------|-------|-------|-------|-------|-------|-------|-------|
| 0x100   | O (Function 1 CSA enable) | O (Function 1 supports CSA) | O (RFU) | Function 1 Standard SDIO Function interface code | |
| 0x101   |       |       |       | Function 1 Extended standard SDIO Function interface code | |
| 0x102   |       |       | O (RFU)| R/W (EPS) | O (SPS) | |
| 0x109-  | Address 0x109: 0x0; Address 0xA0: 0x11; Address 0xB: 0x0 | Pointer to Function 1 CIS | R/W (Supported range: 0-512) | I/O block size for Function 1 | |
| 0x10B   |       |       |       |       |       | Cont'd on next page |
```