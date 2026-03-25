
```markdown
Chapter 6 GPIO Matrix and IO MUX



Figure 6.3-1. Architecture of HP GPIO Matrix, HP IO MUX, LP GPIO Matrix, and LP IO MUX


The following points explain the areas marked numerically in the figure above, taking the HP system as an example.

① Peripheral input signals marked “yes” in column “Direct input through IO MUX” in Table 6.12-1 can be routed to the peripherals via HP IO MUX, or via HP GPIO matrix, while the other input signals can only be routed to the peripherals via HP GPIO matrix.

② There are only 22 inputs from GPIO SYNC to HP GPIO matrix, since ESP32-C61 provides 22 GPIO pins available for users in total.

③ The pins are controlled by the signals: IE, OE, WPU, and WPD.

④ Peripheral outputs marked “yes” in column “Direct output through IO MUX” in Table 6.12-1 can be routed to pins via HP IO MUX or via HP GPIO matrix, while the other output signals can only be routed to pins via HP GPIO matrix.

⑤ There are 22 outputs (corresponding to GPIO pin X: 0~14, 23~28) from HP GPIO matrix to HP IO MUX.

⑥ There are peripheral inputs only through HP IO MUX.

⑦ There are peripheral outputs only through HP IO MUX.



Figure 6.3-2 shows the internal structure of a pad, which is an electrical interface between the chip logic and the GPIO pin. The structure is applicable to all GPIO pins and can be controlled using IE, OE, WPU, and WPD
```