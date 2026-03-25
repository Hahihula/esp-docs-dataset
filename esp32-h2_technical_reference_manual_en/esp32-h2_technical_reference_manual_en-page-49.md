

```markdown
Register 1.14. mip (0x344)

| Bit | Field   | Description                                                                 |
|-----|---------|-----------------------------------------------------------------------------|
| 31  |         | MXP[31:8]                                                                   |
| 7   | MTIP    | Configures the pending status of the machine timer interrupt.<br>0: Not pending<br>1: Pending (R/W) |
| 6   | MXIP[6:5]| Configures the pending status of the 28 external interrupts.<br>0x0: Not pending<br>0x3: Pending (R/W) |
| 5   | UTIP    | Configures the pending status of the user timer interrupt.<br>0: Not pending<br>1: Pending (R/W) |
| 4   | MSIP    | Configures the pending status of the machine software interrupt.<br>0: Not pending<br>1: Pending (R/W) |
| 3   | USIP    | Configures the pending status of the user software interrupt.<br>0: Not pending<br>1: Pending (R/W) |

Register 1.15. ustatus (0x300)

| Bit | Field | Description                                                                 |
|-----|-------|-----------------------------------------------------------------------------|
| 31  |       | (reserved)                                                                  |
| 5   | UPIE   | Write 1 to enable the user previous interrupt (before trap). (R/W)          |
| 4   | (reserved) |                                                                     |
| 3   |        |                                                                     |
| 1   | UIE    | Write 1 to enable the global user mode interrupt. (R/W)                     |
| 0   | Reset  | 0x00000000                                                                   |
```