Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

Subtitle: GoBack

Section Title:
6.2 Peripheral Input via GPIO Matrix

Subsection Title:
6.2.1 Summary

Body Text:
To receive a peripheral input signal via the GPIO Matrix, the GPIO Matrix is configured to source the peripheral signal’s input index (0-18, 23-36, 39-58, 61-90, 95-124, 140-155, 164-181, 190-195, 198-206) from one of the 34 GPIOs (0-19, 21-23, 25-27, 32-39).

The input signal is read from the GPIO pin through the IO MUX. The IO MUX must be configured to set the chosen pin to “GPIO” function. This causes the GPIO pin input signal to be routed into the GPIO Matrix, which in turn routes it to the selected peripheral input.

Subsection Title:
6.2.2 Functional Description

Body Text:
Figure 6.2-1 shows the logic for input selection via GPIO Matrix.

Image Caption (with diagram):
Figure 6.2-1. Peripheral Input via IO MUX, GPIO Matrix

Steps Listed Below Image:

To read GPIO pin X into peripheral signal Y, follow the steps below:

1. Configure the GPIO_FUNC_IN_SEL_CFG register corresponding to peripheral signal Y in the GPIO Matrix:
   - Set GPIO_SIGY_IN_SEL to enable peripheral signal input via GPIO matrix.
   - Set the GPIO_FUNCy_IN_SEL field in this register, corresponding to the GPIO pin X to read from.

2. Configure the GPIO_FUNCx_OUT_SEL_CFG register and clear the GPIO_ENABLE_DATA[x] field corresponding to GPIO pin x in the GPIO Matrix:
   - Set the GPIO_FUNCx_OEN_SEL bit in the GPIO_FUNCx_OUT_SEL_CFG register to force the pin's output state to be determined always by the GPIO_ENABLE_DATA[x] field.
   - The GPIO_ENABLE_DATA[x] field is a bit in either GPIO ENABLE_REG (GPIOs 0-31) or GPIO_ENABLE1_REG (GPIOs 32-39). Clear this bit to disable the output driver for the GPIO pin.

Footer:
Espressif Systems
Page Number: 117

Link Text at Bottom Right Corner:
ESP32 TRM (Version 5.6)

Button Label Below Footer Link:
Submit Documentation Feedback