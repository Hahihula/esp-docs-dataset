

```markdown
Register 4.25. mcontrol (0x7A1)

Continued from the previous page...

u Set this field to make the selected trigger operate in user mode. Operation in user mode is not supported. This field is always 0. (RO)

execute Configures whether to enable the selected trigger to match the virtual address of instructions.
O: Not enable
1: Enable
(R/W)

store Set this field to make the selected trigger match the virtual address of the memory write operation. Not supported by hardware. This field is always 0. (RO)

load Set this field to make the selected trigger match the virtual address of a memory read operation. Not supported by hardware. This field is always 0. (RO)


Register 4.26. maddress (0x7A2)
```
![Register 4.26. maddress (0x7A2) diagram](image)

```markdown
maddress Configures the address used by the selected trigger when performing match operation.
(R/W)

4.6 Performance Counter

The LP CPU implements a clock cycle counter mcycle(h), an instruction counter minstret(h), and 10 event counters mhpmcounter(n:3-12). The clock cycle counter and instruction counter are always available and each is 64-bit wide. Other performance counters are 40-bit wide each.

By default, all counters are enabled after reset. A counter can be enabled or disabled individually via the corresponding bit in the mcontrolinhibit CSR.

As shown in Table 4.6-1, each counter is dedicated to counting a particular event.

Table 4.6-1. Performance Counter

| Counter         | Counted Event                  |
|-----------------|--------------------------------|
| mcycle          | Clock cycles                   |
| minstret        | The number of instructions     |
| mhpmcounter3    | Wait cycles for memory access  |

Espressif Systems
```