

```markdown
## 45.9 Registers

The addresses in this section are relative to Temperature Sensor base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 45.1. APB_SARADC_APB_TSENS_CTRL_REG (0x0058)

| Bit | Description |
|-----|-------------|
| 31  | (reserved)  |
| 23  | APB_SARADC_TSENS_PU |
| 21  | APB_SARADC_TSENS_CLK_DIV |
| 14  | APB_SARADC_TSENS_IN_INV |
| 13  | (reserved)  |
| 8   | APB_SARADC_TSENS_OUT |

0x80 Reset

APB_SARADC_TSENS_OUT Stores the temperature sensor output value. (RO)

APB_SARADC_TSENS_IN_INV Configures whether to invert temperature sensor data.
O: No effect
1: Invert
(R/W)

APB_SARADC_TSENS_CLK_DIV Configures temperature sensor clock division. (R/W)

APB_SARADC_TSENS_PU Configures whether to power up temperature sensor.
O: No effect
1: Power up
(R/W)
```