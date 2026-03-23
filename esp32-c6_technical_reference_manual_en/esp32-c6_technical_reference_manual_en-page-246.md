

```markdown
3. The pins supplied by VDDPST1 or by VDDPST2 are controlled by the signals: IE, OE, WPU, and WPD.
4. Only part of peripheral outputs (marked "yes" in column "Direct output through IO MUX" in Table 7.11-1) can be routed to pins bypassing GPIO matrix. The other output signals can only be routed to pins via GPIO matrix.
5. There are 31 outputs (corresponding to GPIO pin X: 0 ~ 30) from GPIO matrix to IO MUX. Note:
    * For chip variants without an in-package flash, there are 30 outputs (corresponding to GPIO X: 0 ~ 13, 15 ~ 30) from GPIO matrix to IO MUX in total.
    * For chip variants with an in-package flash, there are only 22 outputs (corresponding to GPIO X: 0 ~ 9, 12 ~ 23) from GPIO matrix to IO MUX in total.

Figure 7.3-2 shows the internal structure of a pad, which is an electrical interface between the chip logic and the GPIO pin. The structure is applicable to all 31 GPIO pins and can be controlled using IE, OE, WPU, and WPD signals.

IE
VDD3P3
WPU
Routing to
a peripheral
OE
Buf
Routing from
a peripheral
GND
WPD
Bonding pad

Figure 7.3-2. Internal Structure of a Pad

* IE: input enable
* OE: output enable
* WPU: internal weak pull-up resistor
* WPD: internal weak pull-down resistor
* Bonding pad: a terminal point of the chip logic used to make a physical connection from the chip die to GPIO pin in the chip package

## 7.4 Peripheral Input via GPIO Matrix
```