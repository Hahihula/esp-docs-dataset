

```markdown
## 20.5.2 ICM Register

The addresses in this section are relative to AXI ICM base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 20.72. HP_SYSTEM_ICM_VER_DATE_REG (0x0000)

```
┌───────────────────────────────────────────────┬────────┐
│                   31                     │    0   │
├───────────────────────────────────────────────┼────────┤
│                0x20230214                 │ Reset  │
└───────────────────────────────────────────────┴────────┘

HP_SYSTEM_ICM_VER_DATE Version control register. (R/W)
```

### Register 20.73. HP_SYSTEM_ICM_CLK_EN_REG (0x0004)

```
┌───────────────────────────────────────────────┬────────┐
│                   31                     │    0   │
├───────────────────────────────────────────────┼────────┤
│ (reserved)                                 │ Reset  │
│ 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1 │
└───────────────────────────────────────────────┴────────┘

HP_SYSTEM_ICM_CLK_EN Configures whether or not to force the clock on for the register.
    0: Clock is supported only when application writes registers.
    1: Force clock on for register.
(R/W)
```