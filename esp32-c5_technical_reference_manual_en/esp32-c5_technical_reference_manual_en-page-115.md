

```markdown
Register 2.90. tdata2 (0x7A2)

31                                                                 tdatab2
----------------------------------------------------------------------------------------------------
| Ox00000000 | Reset

tdatab2 Configures the abstract tdatab2 content. This will always be interpreted as maddress since only match type (0x2) triggers are supported. (R/W)


Register 2.91. tdata3 (0x7A3)

31      rvalue   mselect
----------------------------------------------------------------------------------------------------
| 26 | 25 | 24 | Reserved
----------------------------------------------------------------------------------------------------
| 0x0 | 0x0 | 0x0 | Reset

mvalue Data used together with mselect. (R/W)
mselect 0: Ignore mvalue.
1: This trigger will only match if the low bits of mcontext equal mvalue. (R/W)

Reserved Read as 0. (RO)


Register 2.92. tinfo (0x7A4)

31
----------------------------------------------------------------------------------------------------
| 16 | 15 | 0
----------------------------------------------------------------------------------------------------
| 0x0 | Ox0 | Reset

Reserved Read as 0. (RO)

info One bit for each possible type enumerated in tdatab1. Bit N corresponds to type N. If the bit is set, then that type is supported by the currently selected trigger. If the currently selected trigger does not exist, this field contains 1. If the type is not writable, this register may be unimplemented, in which case reading it causes an illegal instruction exception. In this case, the debugger can read the only supported type from tdatab1. (RO)
```