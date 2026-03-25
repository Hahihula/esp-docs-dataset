

```markdown
Register 8.26. IO_MUX_DATE_REG (0x01FC)

IO_MUX_REG_DATE Version control register (R/W)
```

## 8.19.3 GPIO EXT Registers

The addresses in this section are relative to (HP GPIO matrix base address + 0x0F00). GPIO base address is provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section VII .

```markdown
Register 8.27. GPIO_EXT_SIGMADELTA_MISC_REG (0x0004)

GPIO_EXT_SIGMADELTA_CLK_EN Configures whether or not to enable the clock for sigma delta modulation.
O: Not enable
1: Enable
(R/W)
```

```text
31                 0
+------------------+-----------------+
|      (reserved)   |       1        |
+------------------+-----------------+
|                  Reset
```