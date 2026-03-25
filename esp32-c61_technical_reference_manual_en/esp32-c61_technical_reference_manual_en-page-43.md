

```markdown
Register 1.5. mstatus (0x300)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 22  | TW                                                                         |
| 21  | 20                                                                          |
| 18  | MPRV                                                                        |
| 17  | reserved                                                                    |
| 16  | reserved                                                                    |
| 13  | MPP                                                                         |
| 12  | 11                                                                          |
| 10  | 8                                                                           |
| 7   | MPIE                                                                        |
| 6   | (reserved)                                                                  |
| 5   | UPIE                                                                        |
| 4   | MIE                                                                         |
| 3   | (reserved)                                                                  |
| 2   | UIE                                                                         |
| 1   | 0                                                                           |

Reset: 0x000

TW Configures whether the WFI (wait for interrupt) instruction can execute in less privileged modes.
O: WFI can execute in lower privilege modes.
1: WFI can only be executed in machine mode, and if executed in a less privileged mode, it will trigger an illegal instruction exception.
(R/W)

MPRV Configures whether to apply mstatus.MPP as the effective privilege mode, in which loads and stores execute, instead of the actual privilege mode in which the CPU is executing.
O: Not apply
1: Apply
Note that instruction protection is unaffected by this bit.
(R/W)

MPP Configures machine previous privilege mode (before trap).
0x0: User mode
0x3: Machine mode
Note: Only the lower bit is writable. Any write to the higher bit is ignored as it is directly tied to the lower bit.
(R/W)

MPIE Configures whether to enable the machine previous interrupt (before trap).
O: Disable
1: Enable
(R/W)

UPIE Configures whether to enable the user previous interrupt (before trap).
O: Disable
1: Enable
(R/W)

MIE Configures whether to enable the global machine interrupt.
O: Disable
1: Enable
(R/W)

UIE Configures whether to enable the global user interrupt.
O: Disable
1: Enable
(R/W)
```