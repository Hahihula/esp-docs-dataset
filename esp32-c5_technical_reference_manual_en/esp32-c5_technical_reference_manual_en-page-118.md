

```markdown
Register 2.95. mcontrol (0x7A1)

Continued from the previous page...

m Set this field to enable the selected trigger to operate in machine mode. (R/W)
u Set this field to enable the selected trigger to operate in user mode. (R/W)
execute Set this field to enable the selected trigger to fire right before an instruction with the matching virtual address executed by the CPU. (R/W)
store Set this field to enable the selected trigger to fire right before a store operation with the matching data address executed by the CPU. (R/W)
load Set this field to enable the selected trigger to fire right before a load operation with the matching data address executed by the CPU. (R/W)

Register 2.96. maddress (0x7A2)

maddress Configures the address used by the selected trigger when performing a match operation.
This is decoded as NAPOT when match=1 in mcontrol. (R/W)
```