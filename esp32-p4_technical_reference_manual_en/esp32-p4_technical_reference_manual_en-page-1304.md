

```markdown
Register 20.76. HP_SYSTEM_ICM_SYS_ADDRHOLE_INFO_REG (0x003C)
```

| Bit | Field Name | Description |
|-----|------------|-------------|
| 31:8 | (reserved) | Reserved bits, must be written as 0 when writing the register. |
| 7:0 | HP_SYSTEM_ICM_SYS_ADDRHOLE_ID | Records the master ID when ICM_SYS_ADDRHOLE_INT occurs. This ID consists of a 4-bit CID and a 4-bit UID (refer to the related IP for details). The CID is used for master verification in ICM. CID values correspond to the following masters: <br>1: CACHE <br>5: GDMA MST1 <br>6: GDMA MST2 <br>8: AXI GDMA <br>10: DMA2D <br>11: H264 MST1 <br>12: H264 MST2 (RO) |
| 7 | HP_SYSTEM_ICM_SYS_ADDRHOLE_WR | Records the type of transfer when ICM_SYS_ADDRHOLE_INT occurs. <br>O: Read transfer <br>1: Write transfer (RO) |
| 7 | HP_SYSTEM_ICM_SYS_ADDRHOLE_SECURE | Records the type of access error when ICM_SYS_ADDRHOLE_INT occurs. <br>O: Unauthorized access <br>1: Illegal access (RO) |

```markdown
Espressif Systems
```

```markdown
1304
```

```markdown
ESP32-P4 TRM
PRELIMINARY
```

```markdown
Submit Documentation Feedback
```