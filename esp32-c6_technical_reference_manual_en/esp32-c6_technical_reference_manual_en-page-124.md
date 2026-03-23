

```markdown
|31|28|27|26|21|20|19|18|17|16|15|12|11|10|7|6|5|4|3|2|1|0|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| | | | | | | | | | | | | | | | | | | | | | |
|0x2|0|0x0|0|0|0|0|0|0|0001|0|0|0|0|0|0|0|0|0|0|0|Reset|
```

**dmode** Same as `dmode` in `tdat1`. (RO)

**maskmax** Represents the maximum NAPOT range.
- 0: A byte. Only exact match is supported.
- Other values: Not supported.
(RO)

**hit** Not implemented in hardware. This field remains 0. (RO)

**select** Configures to select between an address match or a data match.
- 0: Perform a match on the virtual address
- 1: Perform a match on the data value loaded or stored, or the instruction executed
Note: Only address match is implemented. This field remains 0.
(RO)

**timing** Configures when the trigger will take action.
- 0: Take action before the instruction is executed
- 1: Take action after the instruction is executed
Note: The field remains 0.
(RO)

**sizelo** Only match of any size is supported. This field remains 0. (RO)

**action** Configure action of the selected trigger after it is triggered.
- 0x0: Cause a breakpoint exception
- 0x1: Enter debug mode (Valid only when `dmode = 1`)
Note: Only entering debug mode is supported. This field remains 1.
(RO)

**CHAIN** Not implemented in hardware. This field remains 0. (RO)

**match** Configures the trigger to perform the matching operation of the lower data/instruction address.
- 0x0: Exact match. Namely, the address corresponding to a certain byte during the access must exactly match the value of `maddress`.
- 0x1: NAPOT match. Namely, at least one byte during the access is in the NAPOT region specified in `maddress`.
Note: Only exact byte match is supported. This field remains 0.
(R/W)

**m** Set this field to make the selected trigger operate in machine mode. (RO)

**S** Set this field to make the selected trigger operate in supervisor mode. Operation in supervisor mode is not supported. This field is always 0. (RO)
```