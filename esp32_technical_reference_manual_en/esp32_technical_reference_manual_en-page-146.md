**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Register 6.30. GPIO_PINn_REG (n: 0-19, 21-23, 25-27, 32-39) (0x88+0x4*n)

| Bit | Description |
|-----|-------------|
| 31  | Reserved    |
| ... | ...         |

**GPIO_PINn_INT_ENA**
Interrupt enable bits for pin n: (R/W)
- bit0: APP CPU interrupt enable;
- bit1: APP CPU non-maskable interrupt enable;
- bit2: PRO CPU interrupt enable;
- bit3: PRO CPU non-maskable interrupt enable.

---

### Register 6.31. GPIO_FUNCy_IN_SEL_CFG_REG

| Bit | Description |
|-----|-------------|
| ... | ...         |

**GPIO_PINn_WAKEUP_ENABLE**
GPIO wake-up enable will only wake up the CPU from Light-sleep.
(R/W)

**GPIO_PINn_INT_TYPE**
Interrupt type selection: (R/W)
- 0: GPIO interrupt disable;
- 1: rising edge trigger;
- 2: falling edge trigger;
- 3: any edge trigger;
- 4: low level trigger;
- 5: high level trigger.

---

### Register 6.31. GPIO_PINn_PAD_DRIVER

| Bit | Description |
|-----|-------------|
| ... | ...         |

**GPIO_SIGy_IN_SEL**
Bypass the GPIO Matrix.
- 1: route through GPIO MatrixX
- 0: connect signal directly to peripheral configured in the IO_MUX.

---

**GPIO_FUNCy_IN_INV_SEL**

Invert the input value. 
- 1: invert;
- 0: do not invert (R/W)

---

**GPIO_FUNCy_IN_SEL**
Selection control for peripheral input y.
- A value of 0-39 selects which of the 40 GPIO Matrix input pins this signal is connected to, or Ox38 for a constantly high input or Ox30 for a constantly low input. (R/W)