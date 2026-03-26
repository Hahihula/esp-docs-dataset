

```markdown
Register 1.49. fcsr (0x003)

| Bit | Field | Description |
|-----|-------|-------------|
| 31  |       | (reserved)  |
| 8   | FRM   | Configures the floating-point rounding mode.<br>Valid rounding mode values:<br>0x0: RNE (Round to nearest, ties to even)<br>0x1: RTZ (Round towards zero)<br>0x2: RDN (Round down towards negative infinity)<br>0x3: RUP (Round up towards positive infinity)<br>0x4: RMM (Round to nearest, ties to maximum magnitude)<br>0x5: Reserved (Invalid. Reserved to future use)<br>0x6: Reserved (Invalid. Reserved to future use)<br>0x7: DYN (In Instruction’s rm field, it selects dynamic rounding mode. In the rounding mode register, it is invalid) (R/W) |
| 7   | NV    | Represents the floating-point invalid operation flag. (R/W) |
| 6   | DZ    | Represents the floating-point divide-by-zero flag. (R/W) |
| 5   | OF    | Represents the floating-point overflow flag. (R/W) |
| 4   | UF    | Represents the floating-point underflow flag. (R/W) |
| 3   | NX    | Represents the floating-point inexact flag. (R/W) |
```