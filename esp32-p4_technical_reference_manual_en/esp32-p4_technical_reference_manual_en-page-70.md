

```markdown
Register 1.5. mstatus (0x300)

| SD | (reserved) | TW | (reserved) | MPRV | XS | FS | MPP | (reserved) | MPE | (reserved) | UPIE | MIE | (reserved) | UE |
|----|------------|----|------------|-------|----|----|-----|------------|-----|------------|------|----|------------|----|
| 31 | 30         | 22 | 21         | 18    | 17 | 16 | 15  | 14         | 13  | 12         | 11   | 10 | 9          | 8  |
| 0  | 0x000      | 0  | 0x0        | 0     | 0x0| 0  | 0x0 | 0x0       | 0   | 0x0        | 0    | 0x0| 0          | Reset |

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

XS Represents the combined status of the custom extension states, including the HWLP and the PIE extensions.
0x0: All extension are Off
0x1: None dirty or clean, some on
0x2: None dirty, some clean
0x3: Some dirty
Note that in order to modify the state of either of these extensions, the corresponding CSRs next_hwlp_status and next_pie_status must be used.
(RO)

FS Represents the status of the floating-point unit, including the floating-point registers f0–f31 and the CSRs fcsr, frm, and fflags.
0x0: Off
0x1: Initial
0x2: Clean
0x3: Dirty
(R/W)

MPP Configures machine previous privilege mode (before trap).
0x0: User mode
0x3: Machine mode
Note: Only the lower bit is writable. Any write to the higher bit is ignored as it is directly tied to the lower bit.
(R/W)
```