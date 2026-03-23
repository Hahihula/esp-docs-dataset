

```markdown
Register 5.21. IO_MUX_GPIOn_REG (n: 0-21) (0x0004+4*n)

Continued from the previous page...

IO_MUX_GPIOn_FUN_DRV   Select the drive strength of the pin.

• GPIO2, GPIO3, GPIO5, GPIO18, GPIO18, GPIO19
    0: ~5 mA
    1: ~20 mA
    2: ~10 mA
    3: ~40 mA

• Other GPIOs
    0: ~5 mA
    1: ~10 mA
    2: ~20 mA
    3: ~40 mA

(R/W)

IO_MUX_GPIOn_MCU_SEL   Select IO MUX function for this signal. 0: Select Function 0; 1: Select Function 1; etc. (R/W)

IO_MUX_GPIOn_FILTER_EN Enable filter for pin input signals. 1: Filter enabled; 0: Filter disabled. (R/W)

Register 5.22. IO_MUX_DATE_REG (0x00FC)
```

```markdown
| 31 | 28 | 27 | ... | 0 |
|----|----|----|-----|---|
| 0  | 0  | 0  |     |   |
|    |    |    | 0x2006050 | Reset |

IO_MUX_DATE_REG Version control register (R/W)
```

## 5.15.3 SDM Output Registers

The addresses in this section are relative to (GPIO base address provided in Table 3.3-3 in Chapter 3 System and Memory + 0x0F00).
```