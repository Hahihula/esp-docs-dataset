

```markdown
total.

③ The pins supplied by VDD3P3_CPU or by VDD3P3_RTC are controlled by the signals: IE, OE, WPU, and WPD.

④ Only part of peripheral outputs (marked “yes” in column “Direct output through IO MUX” in Table 5.11-1) can be routed to pins bypassing GPIO matrix. See Table 5.11-1.

⑤ There are only 22 outputs (GPIO pin X: 0 ~ 21) from GPIO matrix to IO MUX.

Figure 5.3-3 shows the internal structure of a pad, which is an electrical interface between the chip logic and the GPIO pin. The structure is applicable to all 22 GPIO pins and can be controlled using IE, OE, WPU, and WPD signals.


![Internal Structure of a Pad](image)

Figure 5.3-3. Internal Structure of a Pad

Note:
• IE: input enable
• OE: output enable
• WPU: internal weak pull-up
• WPD: internal weak pull-down
• Bonding pad: a terminal point of the chip logic used to make a physical connection from the chip die to GPIO pin in the chip package.


## 5.4 Peripheral Input via GPIO Matrix

### 5.4.1 Overview

To receive a peripheral input signal via GPIO matrix, the matrix is configured to source the peripheral input signal from one of the 22 GPIOs (0 ~ 21), see Table 5.11-1. Meanwhile, register corresponding to the peripheral signal should be set to receive input signal via GPIO matrix.
```