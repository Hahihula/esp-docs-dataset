

```markdown
Register 3.25. mcontrol (0x7A1)

Continued from the previous page...

u Set this field to make the selected trigger operate in user mode. Operation in user mode is not supported. This field is always 0. (RO)

execute Configures whether to enable the selected trigger to match the virtual address of instructions.
O: Not enable
1: Enable
(R/W)

store Set this field to make the selected trigger match the virtual address of the memory write operation. Not supported by hardware. This field is always 0. (RO)

load Set this field to make the selected trigger match the virtual address of a memory read operation. Not supported by hardware. This field is always 0. (RO)


Register 3.26. maddress (0x7A2)
```

```markdown
maddress Configures the address used by the selected trigger when performing match operation.
(R/W)

Table 3.7-1. Performance Counter

| Counter          | Counted Event                  |
|------------------|--------------------------------|
| mcycle           | Clock cycles                   |
| minstret         | The number of instructions     |
| mhpmmcounter3    | Wait cycles for memory access  |

Espressif Systems
223
Submit Documentation Feedback
ESP32-P4 TRM
PRELIMINARY
```