**Chapter Title:**
Chapter 10 Timer Group (TIMG)

**Section Header:**
Register 10.9. TIMGn_TxLOAD_REG (x : 0-1) (0x20+0x24*x)

**Field Description and Values Table:**
- **Field Name:** TIMGn_TxLOAD_REG
- **Description:** Write any value to trigger a timer x time-base counter reload. (WO)
- **Register Address:** Register 10.10. TIMGn_WDTCONFIGO_REG (0x0048)

**Table:**
| Bit | Value |
|-----|-------|
| 31  | 0     |
| 30  | 2     |
| 29  | 7     |
| 28  | 6     |
| 27  | 5     |
| 26  | 4     |
| 25  | 3     |
| 24  | 2     |
| 23  | 1     |
| 22  | 0     |
| 21  | 0     |
| 20  | 0     |
| 19  | 0     |
| 18  | 0x1   |
| 17  | 0     |
| 16  | 0     |
| 15  | 0     |
| 14  | Reset |

**Field Descriptions:**
- **TIMGn_WDT_EN:** When set, MWDTS is enabled. (R/W)
- **TIMGn_WDT_STGO:** Stage 0 configuration. O: off; 1: interrupt, 2: reset CPU, 3: reset system. (R/W)
- **TIMGn_WDT_STG1:** Stage 1 configuration. O: off; 1: interrupt, 2: reset CPU, 3: reset system. (R/W)
- **TIMGn_WDT_STG2:** Stage 2 configuration. O: off; 1: interrupt, 2: reset CPU, 3: reset system. (R/W)
- **TIMGn_WDT_STG3:** Stage 3 configuration. O: off; 1: interrupt, 2: reset CPU, 3: reset system. (R/W)
- **TIMGn_WDT_EDGE_INT_EN:** When set, an edge type interrupt will occur at the timeout of a stage configured to generate an interrupt. (R/W)
- **TIMGn_WDT_LEVEL_INT_EN:** When set, a level type interrupt will occur at the timeout of a stage configured to generate an interrupt. (R/W)
- **TIMGn_WDT_CPU_RESET_LENGTH:** CPU reset signal length selection. 0: 100 ns; 1: 200 ns; 2: 300 ns; 3: 400 ns; 4: 500 ns; 5: 800 ns; 6: 1.6 µs; 7: 3.2 µs (R/W)
- **TIMGn_WDT_SYS_RESET_LENGTH:** System reset signal length selection. O: 100 ns, 1: 200 ns, 2: 300 ns, 3: 400 ns; 4: 500 ns, 5: 800 ns, 6: 1.6 µs, 7: 3.2 µs (R/W)
- **TIMGn_WDT_FLASHBOOT_MOD_EN:** When set, Flash boot protection is enabled. (R/W)

**Footer Information:**
Espressif Systems
Page Number: 229
Document Version: ESP32 TRM (Version 5.6)