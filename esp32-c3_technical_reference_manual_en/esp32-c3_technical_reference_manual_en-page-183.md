

```markdown
Register 5.12. GPIO_STATUS_W1TC_REG (0x004C)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 30  |                     |
| 29  |                     |
| 28  |                     |
| 27  |                     |
| 26  |                     |
| 25  |                     |
|     | GPIO_STATUS_W1TC    |
| Value | 0x00000           |
| Reset |                    |

GPIO_STATUS_W1TC   GPIO0 ~ 21 interrupt status clear register. Bit0 ~ bit21 are corresponding to GPIO0 ~ 21, and bit22 ~ bit25 are invalid. If the value 1 is written to a bit here, the corresponding bit in GPIO_STATUS_INTERRUPT will be cleared. Recommended operation: use this register to clear GPIO_STATUS_INTERRUPT. (WT)

Register 5.13. GPIO_PCPU_INT_REG (0x005C)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 30  |                     |
| 29  |                     |
| 28  |                     |
| 27  |                     |
| 26  |                     |
| 25  |                     |
|     | GPIO_PCPU_INT       |
| Value | 0x00000           |
| Reset |                    |

GPIO_PROCPU_INT   GPIO0 ~ 21 PRO_CPU interrupt status. Bit0 ~ bit21 are corresponding to GPIO0 ~ 21, and bit22 ~ bit25 are invalid. This interrupt status is corresponding to the bit in GPIO_STATUS_REG when assert (high) enable signal (bit13 of GPIO_PINn_REG). (RO)
```