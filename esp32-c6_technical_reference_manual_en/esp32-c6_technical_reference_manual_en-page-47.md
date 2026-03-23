

```markdown
Register 1.10. mscratch (0x340)

MSCRATCH

| 31 | 0 |
|-----|----|
|     |    |
| 0x00000000 | Reset |

MSCRATCH Configures machine scratch information for custom use. (R/W)
```

```markdown
Register 1.11. mepc (0x341)

MEPC

| 31 | 0 |
|-----|----|
|     |    |
| 0x00000000 | Reset |

MEPC Configures the machine trap/exception program counter. This is automatically updated with address of the instruction which was about to be executed while CPU encountered the most recent trap. (R/W)
```