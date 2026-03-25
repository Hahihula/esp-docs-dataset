

```markdown
Figure 8.3-1. Architecture of HP GPIO Matrix, HP IO MUX, LP GPIO Matrix, and LP IO MUX


The following points explain the areas marked numerically in the figure above, taking the HP system as an example.

① Peripheral input signals marked “yes” in column “Direct input through HP IO MUX” in Table 8.12-1 can be routed to the peripherals via HP IO MUX, or via HP GPIO matrix, while the other input signals can only be routed to the peripherals via HP GPIO matrix.

② There are only 21 inputs from GPIO SYNC to HP GPIO matrix, since ESP32-C5 provides 21 GPIO pins available for users in total.

③ The pins are controlled by the signals: IE, OE, WPU, and WPD.

④ Peripheral outputs marked “yes” in column “Direct output through HP IO MUX” in Table 8.12-1 can be routed to pins via HP IO MUX or via HP GPIO matrix, while the other output signals can only be routed to pins via HP GPIO matrix.

⑤ There are 21 outputs (corresponding to GPIO pin X: 0~14, 23~28) from HP GPIO matrix to HP IO MUX.
```