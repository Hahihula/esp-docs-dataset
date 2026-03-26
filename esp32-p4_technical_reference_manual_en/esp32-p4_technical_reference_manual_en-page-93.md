

```markdown
Register 1.50. fxsr (0x800)

| 31         | 27   | 26   | 24   | 23   | 22           | 6   | 5   | 4   | 3   | 2   | 1   | 0   |
|------------|------|------|------|------|--------------|-----|-----|-----|-----|-----|-----|-----|
| 0x00000000 | O    | O    | O    |      |              |     |     |     |     |     |     | Reset |

RM   Mapped to frm bits. Write operation to this field will be reflected on fcsr register at the same time. (R/W)

DQNAN Configures the calculated value of QNaN output.
0: The calculated value of QNaN output is the fixed value specified in RISC-V, i.e., 0x7FC00000.
1: The calculated QNaN value is consistent with the IEEE 754 standard.
(R/W)

FE   Floating-point exception accumulation bit. Mapped to FE bits. Write operation to this field will be reflected on fcsr register at the same time.
0: No floating-point exception occurred
1: Floating-point exception occurred
(R/W)

NV   Represents the invalid operand exception flag. Mapped to NV bits. Write operation to this field will be reflected on fcsr register at the same time. (R/W)

DZ   Represents the divide-by-zero exception flag. Mapped to DZ bits. Write operation to this field will be reflected on fcsr register at the same time. (R/W)

OF   Represents the overflow exception flag. Mapped to OF bits. Write operation to this field will be reflected on fcsr register at the same time. (R/W)

UF   Represents the underflow flag. Mapped to UF bits. Write operation to this field will be reflected on fcsr register at the same time. (R/W)

NX   Represents the inexact flag. Mapped to NX bits. Write operation to this field will be reflected on fcsr register at the same time. (R/W)
```

```markdown
Register 1.51. cycle (0xC00)

| 31         | 0   |
|------------|-----|
| 0x00000000 | Reset |

CYCLE Read-only mirror of mcycle. (RO)
```