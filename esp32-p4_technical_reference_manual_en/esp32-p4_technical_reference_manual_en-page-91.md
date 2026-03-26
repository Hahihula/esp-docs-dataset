

```markdown
Register 1.47. fflags (0x001)

NV Represents the floating-point invalid operation flag. (R/W)
DZ Represents the floating-point divide-by-zero flag. (R/W)
OF Represents the floating-point overflow flag. (R/W)
UF Represents the floating-point underflow flag. (R/W)
NX Represents the floating-point inexact flag. (R/W)

Register 1.48. frm (0x002)

FRM Configures the floating-point rounding mode.
Valid rounding mode values:
Ox0: RNE (Round to nearest, ties to even)
Ox1: RTZ (Round towards zero)
Ox2: RDN (Round down towards negative infinity)
Ox3: RUP (Round up towards positive infinity)
Ox4: RMM (Round to nearest, ties to maximum magnitude)
Ox5: Reserved (Invalid. Reserved to future use)
Ox6: Reserved (Invalid. Reserved to future use)
Ox7: DYN (In Instruction's rm field, it selects dynamic rounding mode. In the rounding mode register, it is invalid) (R/W)
```