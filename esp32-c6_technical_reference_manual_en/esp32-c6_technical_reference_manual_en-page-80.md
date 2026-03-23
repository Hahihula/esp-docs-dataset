

```markdown
Register 1.43. mcontrol (0x7A1)

| 31 | 28 | 27 | 26 | 21 | 20 | 19 | 16 | 15 | 12 | 11 | 10 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| 0x2 | 0   | 0xF | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | Reset |

dmode Same as dmode in tdata1. (RW *)

hit This is found to be 1 if the selected trigger had fired previously. This bit is to be cleared manually. (R/W)

action Configures the selected trigger to perform one of the available actions when firing. Valid options are:
Ox0: cause breakpoint exception.
Ox1: enter debug mode (only valid when dmode = 1)
Note: Writing an invalid value will set this to the default value Ox0.
(R/W)

match Configures the selected trigger to perform one of the available matching operations on a data/instruction address. Valid options are:
Ox0: exact byte match, i.e. address corresponding to one of the bytes in an access must match the value of maddress exactly.
Ox1: NAPOT match, i.e. at least one of the bytes of an access must lie in the NAPOT region specified in maddress.
Note: Writing a larger value will clip it to the largest possible value Ox1.
(R/W)

m Set this for enabling selected trigger to operate in machine mode. (R/W)
u Set this for enabling selected trigger to operate in user mode. (R/W)
execute Set this for configuring the selected trigger to fire right before an instruction with matching virtual address is executed by the CPU. (R/W)
store Set this for configuring the selected trigger to fire right before a store operation with matching data address is executed by the CPU. (R/W)
load Set this for configuring the selected trigger to fire right before a load operation with matching data address is executed by the CPU. (R/W)
```