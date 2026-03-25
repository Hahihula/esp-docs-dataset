

```markdown
| 0x00000-0x0000FF | CCCR |
|:------------------|:----------------------------|
| 0x00100-0x0001FF | FBR (Function 1)          |
| 0x00200-0x0002FF | FBR (Function 2)          |
| 0x00300-0x0003FF | FBR (Function 3)          |
| 0x00700-0x0007FF | FBR (Function 7)          |
| 0x00800-0x000FFF | RFU                       |
| 0x01000-0x017FF  | CIS Area                  |
|(common and per-function)||
| 0x018000-0x01FFFF|RFU|

Figure 30.5-3. Function 0 Address Space
```

As defined in the SDIO Specification, CCCR are common control registers, FBR are control configuration registers for each function, and CIS are status registers for storing card information, such as version, power consumption, and manufacturer. The functions of these registers are optional, and are detailed in the SDIO Specification.

The CCCR configuration of ESP32-C61 SDIO slave is shown in Table 30.5-1, and the FBR configuration is shown in Table 30.5-2.

Table 30.5-1. SDIO Slave CCCR Configuration

| Address | Register Name          | Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|:--------|:-----------------------|:------|:------|:------|:------|:------|:---------------------------------------------|:----------------------------------------------|:-----|
| 0x00    | CCCR/SDIO Revision     |       |       | Set SDIO bit[3:0] using HINF_SDIO_VER[7:4] in HINF_CFG_DATA1_REG |       |       | Set CCCR bit[3:0] using HINF_SDIO_VER[3:0] in HINF_CFG_DATA1_REG |       |
| 0x01    | SD Specification Revision |       |       | O (RFU) |       |       | Set SD bit[3:0] using HINF_SDIO_VER[11:8] in HINF_CFG_DATA1_REG |       |
| 0x02    | I/O Enable             |       |       | O (IOE[7:3]) |       |       | R/W (IOE[2:1]) | O (RFU) |
| 0x03    | I/O Ready              |       |       | O (IOR[7:3]) |       |       | R (IOR[2:1]) | O (RFU) |
| 0x04    | Int Enable             |       |       | O (IEN[7:3]) |       |       | R/W (IEN[2:1]) | R/W (IENM) |
| 0x05    | Int Pending            |       |       | O (INT[7:3]) |       |       | R (INT[2:1]) | O (RFU) |
| 0x06    | I/O Abort              |       |       | O (RFU) |       | W (RES) | W (AS[2:0]) |       |
| 0x07    | Bus Interface Control  | R/W (CD Disable) | 1 (SCSI) | R/W (ECSI) | O (RFU) |       | R/W (Bus Width[1:0]) |       |

Cont'd on next page
```