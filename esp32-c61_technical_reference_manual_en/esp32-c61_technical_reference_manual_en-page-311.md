

```markdown
Register 6.39. GPIO_EXT_VERSION_REG (0x01FC)

| 31 | 28 | 27 | ... | 0 |
|----:|----:|----:|-----|---|
|   0 |   0 |   0 |     | Reset |

GPIO_EXT_DATE Version control register.
(R/W)
```

## 6.19.4 LP GPIO Matrix Registers

The addresses in this section are relative to LP GPIO matrix base address provided in Table 4.3-2 in Chapter 4 System and Memory.

For how to program reserved fields, please refer to Section VII .

```markdown
Register 6.40. LP_GPIO_OUT_REG (0x0004)

| 31 | ... | 7 | 6 | ... | 0 |
|----:|-----|---:|---:|-----|---|
|   0 |     | OxO |    | Reset |

LP_GPIO_OUT_DATA_ORIG Configures the output of GPIO0~GPIO6.

The value of each bit can be:
0: Low level
1: High level
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
(R/W/WTC)
```