

# 20.9 Registers

The addresses in this section are relative to ECC Accelerator base address provided in Table 4.3-2 in Chapter 4 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 20.1. ECC_MULT_INT_RAW_REG (0x000C)

```
31
+---------------------------------------------------------------+
| 0 0 0 ... 0 | Reset |
+---------------------------------------------------------------+
```

**ECC_MULT_CALC_DONE_INT_RAW** The raw interrupt status of the `ECC_MULT_CALC_DONE_INT` interrupt. (R/SS/WTC)

## Register 20.2. ECC_MULT_INT_ST_REG (0x0010)

```
31
+---------------------------------------------+
| ... | Reset |
+---------------------------------------------+
```

**ECC_MULT_CALC_DONE_INT_ST** The masked interrupt status of the `ECC_MULT_CALC_DONE_INT` interrupt. (RO)