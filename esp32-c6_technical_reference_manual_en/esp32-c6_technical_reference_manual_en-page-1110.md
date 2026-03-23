

```markdown
| Adress | Register Name         | Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|--------|-----------------------|-------|-------|-------|-------|-------|-------|-------|-------|
| 0x00   | CCCCR/SDIO Revision   |       |       |       |       |       | Set SDIO bit[3:0] using HINF_SDIO_VER[7:4] in HINF_CFG_DATA1_REG | Set CCCR bit[3:0] using HINF_SDIO_VER[3:0] in HINF_CFG_DATA1_REG |
| 0x01   | SD Specification Revision |       |       | O (RFU) |       |       | Set SD bit[3:0] using HINF_SDIO_VER[11:8] in HINF_CFG_DATA1_REG |       |
| 0x02   | I/O Enable            |       |       | O (IOE[7:3]) |       |       | R/W (IOE[2:1]) | O (RFU) |
| 0x03   | I/O Ready             |       |       | O (IOR[7:3]) |       |       | R (IOR[2:1]) | O (RFU) |
| 0x04   | Int Enable            |       |       | O (IEN[7:3]) |       |       | R/W (IEN[2:1]) | R/W (IENM) |
| 0x05   | Int Pending           |       |       | O (INT[7:3]) |       |       | R (INT[2:1]) | O (RFU) |
| 0x06   | I/O Abort             |       |       | O (RFU) | W (RES) |       | W (AS[2:0]) |       |
| 0x07   | Bus Interface Control | R/W (CD Disable) | 1 (SCSI) | R/W (ECSI) | O (RFU) |       |       | R/W (Bus Width[1:0]) |
| 0x08   | Card Capability       | O (4BLS) | O (LSC) | R/W (E4MI) | 1 (S4MI) | O (SBS) | 1 (SRW) | 1 (SMB) | 1 (SDC) |
| 0x09-0x0B | Common CIS Pointer   | Address 0x09: OxO; Address 0xOA: 0x10; Address 0xB: 0x0 (Pointer to card’s common CIS) |       |       |       |       |       |       |
| 0x0C   | Bus Suspend           | O (RFU) |       |       |       |       | O (BR) | O (BS) |
| 0x0D   | Function Select       | O (DF) | O (RFU) |       |       |       | O (FS[3:0]) |       |
| 0x0E   | Exec Flags            |       |       | O (EX[7:1]) |       |       |       | O (EXM) |
| 0x0F   | Ready Flags           |       |       | O (RF[7:1]) |       |       |       | O (RFM) |
| 0x10-0x11 | FNO Block Size      | R/W (Supported range: 0 - 512) (I/O block size for Function 0) |       |       |       |       |       |       |
| 0x12   | Power Control         | O (RFU) |       |       |       |       | R/W (EMPC) | 1 (SMPC) |
```