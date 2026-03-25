

```markdown
Register 1.5. mstatus (0x300)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | TW | (reserved) | MPP | (reserved) | MPE | (reserved) | UP|E | (reserved) | UE |
|-----:|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:--|:------------|:----|:------------|:----|:------------|:--|:------------|:---|
| 0x000 |     | O   |     | 0x00 |      |      |      |      |      |      | O   |    |            | O×O |            | O   |            | O×E |            | O |
```

UIE Write 1 to enable the global user mode interrupt. (R/W)

MIE Write 1 to enable the global machine mode interrupt. (R/W)

UPIE Write 1 to enable the user previous interrupt (before trap). (R/W)

MPIE Write 1 to enable the machine previous interrupt (before trap). (R/W)

MPP Configures machine previous privilege mode (before trap).

Ox0: User mode

Ox3: Machine mode

Note: Only the lower bit is writable. Any write to the higher bit is ignored as it is directly tied to the lower bit.

(R/W)

TW Configures whether to cause illegal instruction exception when WFI (Wait-for-Interrupt) instruction is executed in U mode.

0: Executing WFI instruction will not cause illegal exception in U mode

1: Executing WFI instruction in U mode will cause illegal instruction exception

(R/W)
```