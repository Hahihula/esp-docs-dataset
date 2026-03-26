

```markdown
Register 1.65. mext_pie_status (0x7F2)

STATE Configures the state of the PIE extension:
- 0x0: OFF (Executing PIE instructions will trigger illegal instruction exception)
- 0x1: INITIAL
- 0x2: CLEAN
- 0x3: DIRTY

This is the extension state bits for the PIE extension, with similar functionality as the mstatus.FS bits of RV32F. Please refer to the "RISC-V Volume II - Privileged Architecture" for the standard interpretation of the STATE values.
(R/W)
```

```markdown
Register 1.66. jvt (0x017)

BASE Represents jump table base address. (R/W)

MODE Represents configurable modes. This field is reserved to define the usage of this register.
Currently, only one usage is defined, i.e., jump table. Other usages are reserved for future use).
- 0x0: The JTV_BASE is used as jump table
Others: reserved for future standard use
(R/W)
```