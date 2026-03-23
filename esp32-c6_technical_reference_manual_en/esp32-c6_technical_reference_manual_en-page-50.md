

```markdown
Register 1.14. mip (0x344)

| Bit | Field   | Description                                                                 |
|-----|---------|-----------------------------------------------------------------------------|
| 31  |         | Reset                                                                       |
|     | 0x0     |                                                                             |
| 8-7 | MTP     |                                                                             |
| 6-5 | MXIP[6:5]|                                                                             |
| 4   | UTIP    | Configures the pending status of the user timer interrupt.<br>0: Not pending<br>1: Pending (R/W) |
| 3   | MSIP    | Configures the pending status of the machine software interrupt.<br>0: Not pending<br>1: Pending (R/W) |
| 2-1 | MXIP[2:1]|                                                                             |
| 0   | USIP    | Configures the pending status of the user software interrupt.<br>0: Not pending<br>1: Pending (R/W) |

Register 1.15. ustatus (0x300)

| Bit | Field     | Description                                                                 |
|-----|-----------|-----------------------------------------------------------------------------|
| 31  |           | Reset                                                                       |
|     | 0x0000000 |                                                                             |
| 5   | UPIE      | Write 1 to enable the user previous interrupt (before trap). (R/W)          |
| 4-3 | (reserved)|                                                                             |
| 1   | UIE       | Write 1 to enable the global user mode interrupt. (R/W)                     |
```