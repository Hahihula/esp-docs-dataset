

```markdown
Register 52.55. EMACNSUPT_REG (0x0714)

ADDSSUB with Configures whether to subtract or add the system time value the contents of the update register.
O: Add
1: Subtract
(R/W)

TSSSUPD Configures the sub-second representation of time, with an accuracy of 0.46 ns.

When EMACTSTPCTRL_REG[9] (TSCTRLLSSR) is set, each bit represents 1 ns and the programmed value should not exceed 0x3B9A_C9FF. (R/W)
```

```markdown
Register 52.56. EMACTSTPADDEND_REG (0x0718)

TSAR Configures the 32-bit time value to be added to the Accumulator register to achieve time synchronization. (R/W)
```

```markdown
Register 52.57. EMACTGTIME2ND_REG (0x071C)

TSTR Configures the target time.
Measurement unit: second.

When the system time matches or exceeds the target time, an interrupt is generated (if enabled).
(R/W)
```