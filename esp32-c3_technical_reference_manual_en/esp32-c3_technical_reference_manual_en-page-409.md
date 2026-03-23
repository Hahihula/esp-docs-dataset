

```markdown
Register 14.83.EXTMEM_IBUS_PMS_TBL_ATTR_REG (0x00E8)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| 0   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | (reserved) | Oxf | Oxf | Reset |

EXTMEM_IBUS_PMS_SCT1_ATTR Configures IBUS' access to Cache IBUS Region1.
Bit 0: Instruction execution access in the privileged environment
Bit 1: Read access in the privileged environment
Bit 2: Instruction execution access in the unprivileged environment
Bit 3: Read access in the unprivileged environment
(R/W)

EXTMEM_IBUS_PMS_SCT2_ATTR Configures IBUS' access to Cache IBUS Region2.
Bit 0: Instruction execution access in the privileged environment
Bit 1: Read access in the privileged environment
Bit 2: Instruction execution access in the unprivileged environment
Bit 3: Read access in the unprivileged environment
(R/W)
```