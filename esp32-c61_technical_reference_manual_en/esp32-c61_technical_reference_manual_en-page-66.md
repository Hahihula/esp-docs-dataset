

```markdown
Register 1.59. jvt (0x017)

| Bits | Description                                                                 |
|------|-----------------------------------------------------------------------------|
| 31   | BASE                                                                        |
|      |                                                                             |
| 6    | MODE                                                                       |
| 5    |                                                                             |
| 0    | Reset                                                                      |

BASE Represents jump table base address. (R/W)

MODE Represents configurable modes. This field is reserved to define the usage of this register.
Currently, only one usage is defined, i.e., jump table. Other usages are reserved for future use.
0x0: The JTV_BASE is used as jump table
Others: reserved for future standard use
(R/W)
```