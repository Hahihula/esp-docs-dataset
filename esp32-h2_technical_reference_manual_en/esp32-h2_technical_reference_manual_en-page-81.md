

```markdown
# 1.13 Dedicated IO

## 1.13.1 Overview

Normally, GPIOs are an APB peripheral, which means that changes to outputs and reads from inputs can get stuck in write buffers or behind other transfers, and in general are slower because generally the APB bus runs at a lower speed than the CPU. As an alternative, the CPU core implements I/O processors specific CPU registers (CSRs) which are directly connected to the GPIO matrix or IO pads. As these registers can get accessed in one instruction, speed is fast.

## 1.13.2 Features

- 8 dedicated IOs directly mapped on GPIOs
- No latency for driving output ports
- Two CPU cycle latency for sensing input values

## 1.13.3 Functional Description

The CPU core has a set of 8 inputs and outputs (pin value + pin output enable). These input and output ports are directly connected to the GPIO matrix, through which they can be mapped on top-level pads. Please refer to Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX) for more details.

The CPU implements three custom CSRs:

- GPIO_IN is read-only and reflects the input value.
- GPIO_OUT is R/W and reflects the output value for the GPIOs.
- GPIO_OEN is R/W and reflects the output enable state for the GPIOs. It controls the pad direction. Programming high would mean the pad should be configured in output mode. Programming low means it should be configured in input mode.
```