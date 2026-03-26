

```markdown
Chapter 9 GPIO Matrix and IO MUX

GoBack

9.12-1) can be routed to the peripherals via HP IO MUX, or via HP GPIO matrix, while the other input signals can only be routed to the peripherals via HP GPIO matrix.

• ② There are only 55 inputs from GPIO SYNC to HP GPIO matrix, since ESP32-P4 provides 55 GPIO pins in total.  
• ③ The pins supplied by VDD_IO_0, VDD_FLASHIO, VDD_IO_4 ~ VDD_IO_6, and VDD_LP are controlled by the signals: IE, OE, HYS, WPU, and WPD.  
• ④ Part of peripheral outputs (marked “yes” in column “Direct output through HP IO MUX” in Table 9.12-1) can be routed to pins via HP IO MUX or via HP GPIO matrix, while the other output signals can only be routed to pins via HP GPIO matrix.  
• ⑤ There are 55 outputs (corresponding to GPIO pin X: 0 ~ 54) from HP GPIO matrix to HP IO MUX.  
• ⑥ There are peripheral inputs only through HP IO MUX.  
• ⑦ There are peripheral outputs only through HP IO MUX.

Figure 9.3-2 shows the internal structure of a pad, which is an electrical interface between the chip logic and the GPIO pin. The structure is applicable to all 55 GPIO pins and can be controlled using IE, OE, WPU, and WPD signals. For the configuration of these signals, see IO_MUX_GPIOx_REG or LP_IOMUX_PADx_REG.

![Internal Structure of a Pad](#)  
Figure 9.3-2. Internal Structure of a Pad

• IE: input enable  
• OE: output enable  
• WPU: internal weak pull-up resistor  
• WPD: internal weak pull-down resistor  
• Bonding pad: a terminal point of the chip logic used to make a physical connection from the chip die to GPIO pin in the chip package
```