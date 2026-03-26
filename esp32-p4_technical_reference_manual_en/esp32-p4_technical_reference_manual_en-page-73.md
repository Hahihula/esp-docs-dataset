

```markdown
## Register 1.7. mideleg (0x303)

```
31                                 0
+----------------------------------------------------------+
|                0x00000000               | Reset |
+----------------------------------------------------------+

mideleg All bits are hardwired to 0 since only CLIC mode is available. (RO)
```

## Register 1.8. mie (0x304)

```
31                                 0
+----------------------------------------------------------+
|                0x00000000               | Reset |
+----------------------------------------------------------+

mie All bits are hardwired to 0 since only CLIC mode is available. (RO)
```

## Register 1.9. mtvec (0x305)

```
31                                 BASE           MODE
+-----------------------------------------------------------------------------+
|                0x000000 | 6 5   2 1 0 | Reset |
+-----------------------------------------------------------------------------+

BASE Configures the higher 26 bits of exception and non-vectored machine mode interrupt base address aligned to 64 bytes. (R/W)

MODE Represents whether machine mode interrupts are operating in CLIC mode or vectored/non-vectored CLINT mode. Only CLIC mode 0x3 is available. (RO)
```

## Register 1.10. mtvt (0x307)

```
31                                 BASE           reserved
+-----------------------------------------------------------------------------+
|                0x000000 | 6 5   2 1 0 | Reset |
+-----------------------------------------------------------------------------+

BASE Configures the higher 26 bits of CLIC machine mode interrupt vector base address aligned to 64 bytes. (R/W)
```