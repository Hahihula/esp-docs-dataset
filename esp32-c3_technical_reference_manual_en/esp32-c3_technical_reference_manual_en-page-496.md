

```markdown
Chapter 19 HMAC Accelerator (HMAC)    GoBack


# 19.5 Registers

The addresses in this section are relative to HMAC Accelerator base address provided in Table 3.3-3 in Chapter 3 System and Memory.

## Register 19.1. HMAC_SET_START_REG (0x0040)

```
┌───────────────────────────────────────────────┬────┐
│ 31 30 29 28 ... 07 06 05 04 03 02 01 00 │ 1  0 │
├───────────────────────────────────────────────┼────┤
│ (reserved)                                   │ Reset│
└───────────────────────────────────────────────┴────┘
```

**HMAC_SET_START** Set this bit to enable HMAC. (WO)

## Register 19.2. HMAC_SET_PARA_FINISH_REG (0x004C)

```
┌───────────────────────────────────────────────┬────┐
│ 31 30 29 28 ... 07 06 05 04 03 02 01 00 │ 1  0 │
├───────────────────────────────────────────────┼────┤
│ (reserved)                                   │ Reset│
└───────────────────────────────────────────────┴────┘
```

**HMAC_SET_PARA_END** Set this bit to finish HMAC configuration. (WO)

## Register 19.3. HMAC_SET_MESSAGE_CALC_BLOCK_REG (0x0050)

```
┌───────────────────────────────────────────────┬────┐
│ 31 30 29 28 ... 07 06 05 04 03 02 01 00 │ 1  0 │
├───────────────────────────────────────────────┼────┤
│ (reserved)                                   │ Reset│
└───────────────────────────────────────────────┴────┘
```

**HMAC_SET_TEXT_ONE** Call SHA to calculate one message block. (WO)
```