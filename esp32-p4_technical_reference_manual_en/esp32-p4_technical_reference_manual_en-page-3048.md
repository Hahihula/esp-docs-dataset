

```markdown
Register 62.20. ADC_DMA_CONF_REG (0x0060)

| 31 | 30 | 29 | ... | 16 | 15 | ... | 0 |
|----|----|----|-----|----|----|-----|---|
| 0  | 0  | 0  | ... | 0  | 0  | ... | Reset |

ADC_APB_ADC_EOF_NUM Configures the number of samples. When the sampling reaches the configured number, the EOF flag bit sent to GDMA will be pulled high. (R/W)

ADC_APB_ADC_RESET_FSM Configures whether to reset the status of HP ADC controller.
- 0: No effect
- 1: Reset
(R/W)

ADC_APB_ADC_TRANS Configures whether to let HP ADC controller use GDMA.
- 0: No effect
- 1: HP ADC controller uses DMA
(R/W)

Register 62.21. ADC_CTRL_DATE_REG (0x03FC)

| 31 | 30 | ... | 0 |
|----|----|-----|---|
| 0  |    | Ox2212260 | Reset |

ADC_CTRL_DATE HP ADC version control register. (RO)
```

## 62.10.2 LP ADC Registers

The addresses in the following section are relative to LP ADC’s base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.
```