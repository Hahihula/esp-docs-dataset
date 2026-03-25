

```markdown
Register 2.95. mcontrol (0x7A1)

| 31 | 28 | 27 | 26 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 12 | 11 | 10 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| 0x2 | 0   | 0x8 |     | O   | O   | O   | (reserved) | timing | sizelo | action | (reserved) | match | m    | u    | execute | store | load |
| Reset |

dmode Same as dmode in tdatal. (RW*)

maskmax Represents the largest natural power-of-two (NAPOT) range supported when match is 1.
It is always read as 0x8, which means only the lowest 8 bits can be masked. (RO)

hit This is found to be 1 if the selected trigger had fired previously. This bit needs to be cleared manually. (R/W)

timing Set this field to enable load/store trigger action timing.
0: Action for this trigger will be taken just before the instruction that triggered it is executed, but after all preceding instructions are committed.
1: Action for this trigger will be taken after the instruction that triggered it is executed. It should be taken before the next instruction is executed.
(R/W)

sizelo This field contains the lowest two bits of access address.
0x0: The trigger will attempt to match against an access of any size
0x1: The trigger will attempt to match against 8-bit memory accesses
0x2: The trigger will attempt to match against 16-bit memory accesses
0x3: The trigger will attempt to match against 32-bit memory accesses
(R/W)

action Configures the selected trigger to perform one of the available actions when firing. Valid options are:
0x0: cause breakpoint exception.
0x1: enter debug mode (only valid when dmode = 1)
0x2: Enable trace on trigger[0] hit
0x3: Enable trace on trigger[1] hit
0x4: Enable trace on trigger[2] hit
Note: Writing an invalid value will set this to the default value 0x0.
(R/W)

match Configures the selected trigger to perform one of the available matching operations on a data/instruction address. Valid options are:
0x0: exact byte match, i.e. address corresponding to one of the bytes in an access must match the value of maddress exactly.
0x1: NAPOT match, i.e. at least one of the bytes of an access must lie in the NAPOT region specified in maddress.
Note: Writing a larger value will clip it to the largest possible value 0x1.
(R/W)

Continued on the next page...
```