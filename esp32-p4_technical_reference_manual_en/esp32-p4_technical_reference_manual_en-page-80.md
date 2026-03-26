

```markdown
Register 1.22. ustatus (0x0000)

| SD | (reserved) | TW | (reserved) | MPRV | XS | FS | MPP | (reserved) | MPE | (reserved) | UPPIE | MIE | (reserved) | UE |
|----|------------|----|------------|-------|----|----|-----|------------|-----|------------|-------|------|------------|----|
| 31 | 30         | 22 | 21         | 20    | 18 | 17 | 16  | 15         | 14  | 13         | 12    | 11   | 10         | 9  |
| 0  | 0x000      | 0  | 0x0        | 0     | 0  | 0x0 | 0x0 | 0x0       | 0x0 | 0x0        | 0x0   | 0x0  | 0x0        | Reset |

SD Automatically set when either the FS or XS fields signal the presence of some dirty state that will require saving extension context to memory. (RO)

TW Represents whether the WFI (wait for interrupt) instruction can execute in less privileged modes.
O: WFI can execute in lower privilege modes.
1: WFI can only be executed in machine mode, and if executed in a less privileged mode, it will trigger an illegal instruction exception.
(RO)

MPRV Represents whether to apply ustatus.MPP as the effective privilege mode, in which loads and stores execute, instead of the actual privilege mode in which the CPU is executing.
O: Not apply
1: Apply
Note that instruction protection is unaffected by this bit.
(RO)

XS Represents the combined status of the custom extension states, including the HWLP and the PIE extensions.
Ox0: All extension are Off
Ox1: None dirty or clean, some on
Ox2: None dirty, some clean
Ox3: Some dirty
Note that in order to modify the state of either of these extensions, the corresponding CSRs next_hwlp_status and next_pie_status must be used.
(RO)

FS Configures the status of the floating-point unit, including the floating-point registers f0–f31 and the CSRs fcsr, frm, and fflags.
Ox0: Off
Ox1: Initial
Ox2: Clean
Ox3: Dirty
(R/W)

MPP Represents machine previous privilege mode (before trap).
Ox0: User mode
Ox3: Machine mode
Note: Only the lower bit is writable. Any write to the higher bit is ignored as it is directly tied to the lower bit.
(RO)
```