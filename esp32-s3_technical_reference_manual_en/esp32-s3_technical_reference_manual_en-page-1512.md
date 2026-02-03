**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

---

**Section Header (Register):**
Register 39.68. APB_SARADC_DMA_CONF_REG (0x006C)

**Binary Representation Diagram for Register 39.68:**

```
| 31 | 30 | 29 | ... | 15 | 14 | 13 | 12 | 11 | 10 | 9  |
|----|----|----|-----|-----|-----|-----|-----|-----|-----|----|
|     |     |     |     |     |     |     |     |     |     |    |
| Reserved |      |      |      |      |      |      |      |      |      | 0   |
```

**Description for Register 39.68:**
- APB_SARADC_APB_ADC_EOF_NUM
- DMA_IN_SUC_EOF is generated when the sample count is equal to apbadc_eof_num.
- (R/W)

- APB_SARADC_APB_ADC_RESET_FSM
- Reset DIG ADC controller status.

**Binary Representation Diagram for Register 39.68:**

```
| 25 | 24 | ... | 16 | 15 |
|----|----|-----|-----|-----|
|     |     |     |     |     |
| Reserved |      |      |      |      | Reset
```

---

**Section Header (Register):**
Register 39.69. APB_SARADC_APB_ADC_CLKM_CONF_REG (0x0070)

**Binary Representation Diagram for Register 39.69:**

```
| 31 | 23 | ... | 20 | 19 | 14 | 13 | 12 | 8  |
|----|----|-----|-----|-----|-----|-----|-----|----|
|     |     |     |     |     |     |     |     |    |
| Reserved |      |      |      |      |      |      |      |    |
```

**Description for Register 39.69:**
- APB_SARADC_CLKM_DIV_NUM
- The integer part of ADC clock divider.
- Divider value = APB_SARADC_CLKM_DIV_NUM + APB_SARADC_CLKM_DIV_B/APB_SARADC_CLKM_DIV_A.

**Binary Representation Diagram for Register 39.69:**

```
| 4 | ... |
|----|
|     |
| Reserved
```

- (R/W)

- APB_SARADC_CLKM_DIV_B
- The numerator value of fractional clock divider.
- (R/W)

- APB_SARADC_CLKM_DIV_A
- The denominator value of fractional clock divider. 
- (R/W)

- APB_SARADC_CLKM_SEL
- Select clock source: 0: clock off; 1: select PLL_D2_CLK as the clock source.
- (R/W)

**Source Note for Register 39.69:**
source. 2: select APB_CLK as the clock source.

---

**Footer Information:** 
Espressif Systems
Page number: 1512
Document version and type information:
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback