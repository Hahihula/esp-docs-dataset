

```markdown
Register 3.23. tdata1 (0x7A1)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | ... | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|-----|---|---|---|---|---|
|     |    |    |    | type | dmode |      | x   | 1 | 0 | Reset |

type Represents the trigger type. This field is reserved since only match type (0x2) triggers are supported. (RO)

dmode This is set to 1 if a trigger is being used by the debugger. This field is reserved since it is only supported in debug mode. (RO)

data Configures the abstract tdata1 content. This will always be interpreted as fields of mcontrol since only match type (0x2) triggers are supported. (R/W)
```

```markdown
Register 3.24. tdata2 (0x7A2)

| Bit | 31 | ... | 0 |
|-----|----|-----|---|
|     |    |      | Reset |

tdata2 Configures the abstract tdata2 content. This will always be interpreted as maddress since only match type (0x2) triggers are supported. (R/W)
```