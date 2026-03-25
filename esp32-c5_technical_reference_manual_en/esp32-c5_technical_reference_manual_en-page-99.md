

```markdown
Register 2.80. pmpXcfg

| 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|---|---|---|---|---|---|---|---|
|   | XL| A | X | W | R |    | Reset |
| 0 | 0 | 0 | 0 | 0 | 0 | 0 |     |

L Configures lock bit. Once set, it can only be cleared through a core reset. (R/W)

XL Configures custom-lock bit. Once set, it can only be cleared through a core reset. O: PMP CSR accesses work normally
1: Respective pmpaddr and pmcfg entry is locked and cannot be modified (R/W)

A Configures address matching mode.
0: OFF
1: TOR (Top of range)
2: Not Supported
3: NAPOT (Natullary aligned power-of-two region >= 128 Bytes) (R/W)

X Configures execute permission. When set, execution from the address range is allowed. (R/W)

W Configures write permission. When set, memory writes to the address range are allowed. (R/W)

R Configures execute permission. When set, memory reads from the address range are allowed. (R/W)


Register 2.81. pmpaddrn (n: 0-15) (0x3B0+0x1*n)
```

```markdown
address Configures the address for pmpaddrn. (R/W)
```