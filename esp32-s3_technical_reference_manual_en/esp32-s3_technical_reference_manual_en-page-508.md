**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Register 6.20. GPIO_FUNCx_OUT_SEL_CFG_REG (X: 0-48) (0x0554+0x4\*X)

| Field | Description |
|-------|-------------|
| 31    | Reserved |
| ...   | ...         |

**GPIO_FUNCx_OUT_SEL**
Selection control for GPIO output X. If a value Y (0<=Y<256) is written to this field, the peripheral output signal Y will be connected to GPIO output X.

If a value 256 is written to this field, bit X of GPIO_OUT_REG/GPIO_OUT1_REG and GPIO_ENABLE_REG/GPIO ENABLE1 REG will be selected as the output value and output enable. (R/W)

**GPIO_FUNCx_OUT_INV_SEL**
0: Do not invert the output value; 1: Invert the output value.

**GPIO_FUNCx_OEN_SEL**
Use output enable signal from peripheral; 1: Force the output enable signal to be sourced from GPIO_ENABLE_REG [X]. (R/W)

**GPIO_FUNCn_OEN_INV_SEL**
0: Do not invert the output enable signal; 1: Invert the output enable signal. (R/W)

---

### Register 6.21. GPIO_CLOCK_GATE_REG (0x062C) 

| Field | Description |
|-------|-------------|
| 31    | Reserved |
| ...   | ...         |

**GPIO_CLK_EN**
Clock gating enable bit. If set to 1, the clock is free running.

---

### Register 6.22. GPIO_STATUS_REG (0x0044)

| Field | Description |
|-------|-------------|
| 31    | Reserved |
| ...   | ...         |

**GPIO_STATUS_INTERRUPT**
GPIO0 ~ 31 interrupt status register.
(R/W) 

---

*Espressif Systems*
*Submit Documentation Feedback*

ESP32-S3 TRM (Version 1.7)

---