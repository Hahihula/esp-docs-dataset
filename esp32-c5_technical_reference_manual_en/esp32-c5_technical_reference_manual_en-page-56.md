

```markdown
Register 2.5. mstatus (0x300)

| SD | (reserved) | TW | (reserved) | MPRV | reserved | reserved | MPP | (reserved) | MPE | (reserved) | UPME | (reserved) | UE |
|----|------------|-----|------------|-------|----------|----------|-----|------------|-----|------------|------|------------|----|
| 31 | 30         | 22  | 21         | 18    | 17       | 16       | 15  | 14         | 13  | 12         | 11   | 10         | 9   |
| 0  | 0x000      | 0   | 0x0        | 0     | 0x0      | 0x0      | 0x0 | 0          | 0   | 0x0        | 0     | 0x0        | Reset |

SD Automatically set when either the FS or XS fields signal the presence of some dirty state that will require saving extension context to memory. (RO)

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

Continued on the next page...

Register 2.5. mstatus (0x300)

Continued from the previous page...

MPIE Write 1 to enable the machine previous interrupt (before trap). (R/W)

UPIE This is hardwired to 0 as user mode interrupts are not supported. (RO)

MIE Write 1 to enable the global machine mode interrupt. (R/W)

UIE This is hardwired to 0 as user mode interrupts are not supported. (RO)
```