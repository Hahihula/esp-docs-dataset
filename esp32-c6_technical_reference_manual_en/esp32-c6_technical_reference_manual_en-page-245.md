

```markdown
- perform GPIO function routed by GPIO matrix;
- or perform direct connection bypassing GPIO matrix.
LP IO MUX has the following feature:
• Control of eight LP GPIO pins (GPIO0 ~ GPIO7) that can be used by the peripherals in ULP and LP system.

## 7.3 Architectural Overview

Figure 7.3-1 shows in details how GPIO matrix, IO MUX, and LP IO MUX route signals from pins to peripherals, and from peripherals to pins.

**Figure 7.3-1. Architecture of IO MUX, LP IO MUX, and GPIO Matrix**

1. Only part of peripheral input signals (marked “yes” in column “Direct input through IO MUX” in Table 7.11-1) can bypass GPIO matrix. The other input signals can only be routed to peripherals via GPIO matrix.
2. There are only 31 inputs from GPIO SYNC to GPIO matrix, since ESP32-C6 provides 31 GPIO pins in total.

Note:
• For chip variants without an in-package flash, there are 30 inputs from GPIO SYNC to GPIO matrix in total. GPIO14 is not led out to any chip pins.
• For chip variants with an in-package flash, there are only 22 inputs from GPIO SYNC to GPIO matrix in total. GPIO10 ~ GPIO11 are not let out to chip pins, and GPIO24 ~ GPIO30 are used to connect the in-package flash.
```