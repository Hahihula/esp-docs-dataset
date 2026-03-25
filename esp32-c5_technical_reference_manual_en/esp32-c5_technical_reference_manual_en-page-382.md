

```markdown
Register 8.58. LP_IO_MUX_GPIOn_REG (n: 0-7) (0x0000+0x4*n)

Continued from the previous page...

LP_IO_MUX_GPIOn_HYS_SEL Configures to choose the signal for enabling the hysteresis function for GPIO n.

0: Choose the output enable signal of eFuse
1: Choose the output enable signal of LP_IO_MUX_GPIOn_HYS_EN
(R/W)
```

```markdown
Register 8.59. LP_IO_MUX_DATE_REG (0x01FC)

LP_IO_MUX_REG_DATE

(reserved) 31 28 27 0
+-----------------------------+
| O   O   O                   | 0x2211270 Reset
+-----------------------------+

LP_IO_MUX_REG_DATE Version control register.
(R/W)
```