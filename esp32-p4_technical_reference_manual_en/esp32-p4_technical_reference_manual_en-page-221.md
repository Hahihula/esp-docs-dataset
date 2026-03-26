

```markdown
Register 3.22. tselect (0x7A0)

tselect Configures the index of the selected trigger unit. (R/W)


Register 3.23. tdata1 (0x7A1)

type | dmode | data
-----|-------|------
31   | 28    | 26
0    | 0     | 1 0 x 1 0 4 0

type Represents the trigger type. This field is reserved since only match type (0x2) triggers are supported. (RO)

dmode This is set to 1 if a trigger is being used by the debugger. This field is reserved since it is only supported in debug mode. (RO)

data Configures the abstract tdata1 content. This will always be interpreted as fields of mcontrol since only match type (0x2) triggers are supported. (R/W)


Register 3.24. tdata2 (0x7A2)

tdata2

0

tdata2 Configures the abstract tdata2 content. This will always be interpreted as maddress since only match type (0x2) triggers are supported. (R/W)
```