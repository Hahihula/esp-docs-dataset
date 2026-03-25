

```markdown
- 77 HP peripheral output signals routed to the output of any GPIO pins
- Signal synchronization for HP peripheral inputs based on **HP IO MUX** operating clock
- GPIO Filter hardware for input signal filtering
- Glitch Filter hardware for second-time filtering on input signal
- Sigma delta modulated (SDM) output
- GPIO simple input and output
- HP GPIO Wakeup

HP IO MUX has the following features:

* Control of 21 GPIOs (GPIO0~GPIO14, GPIO23~GPIO28) for HP peripherals.
* A configuration register **IO_MUX_GPIOn_REG** provided for each GPIO pin, to control the pin’s input/output, pull-up/pull-down, drive strength, and function selection.
* Better high-frequency digital performance achieved by routing some digital signals (such as SPI) directly from HP IO MUX to peripherals.

### 8.2.2 LP GPIO Matrix and LP IO MUX

LP GPIO matrix has the following features:

- GPIO simple input and output
- LP GPIO Wakeup

LP IO MUX has the following feature:

* Control of 7 LP GPIO pins (GPIO0~GPIO6) for LP peripherals.
* A configuration register **LP_IO_MUX_GPIOn_REG** provided for each LP GPIO pin, to control the pin’s input/output, pull-up/pull-down, drive strength, and function selection.
* A field **LP_AON_GPIO_MUX_SEL** provided to select the source of the pin control signals, from HP IO MUX or LP IO MUX.

## 8.3 Architectural Overview

Figure 8.3-1 shows in details how HP GPIO matrix, HP IO MUX, LP GPIO matrix, and LP IO MUX route signals from pins to peripherals, and from peripherals to pins.
```