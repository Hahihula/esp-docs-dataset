**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**GoBack Link**

**Note Section:**
The peripheral output signals 224 to 228 can be configured to be routed in from one GPIO and output directly from another GPIO.

**Section Heading:**
6.3.2 Functional Description

**Body Text:**
One of the 176 output signals can be selected to go through the GPIO matrix into the IO MUX and then to a pin.
Figure 6.3-1 illustrates the configuration.

**Image Caption (Diagram):**
Figure 6.3-1. Output via GPIO Matrix

**Steps for Outputting Peripheral Signal:**

To output peripheral signal Y to particular GPIO pin X, follow these steps:

1. Configure the GPIO_FUNC_X_OUT_SEL register and GPIO_ENABLE_DATA[x] field corresponding to GPIO X in the GPIO Matrix:
   - Set the GPIO_FUNCx_OUT_SEL field in GPIO_FUNCx_OUT_SEL_CFG to the numeric index (Y) of desired peripheral output signal Y.
     * If the signal should always be enabled as an output, set the GPIO_FUNCx_OEN_SEL bit in the GPIO_FUNCx_OUT_SEL_CFG register and the GPIO_ENABLE_DATA[x] field in the GPIO_ENABLE_REG register corresponding to gpio pin x. To have the output enable signal decided by internal logic, clear the GPIO_FUNCx_OEN_SEL bit instead.
   - The GPIO_ENABLE_DATA[x] field is a bit in either GPIO_ENABLE_G (GPIOs 0-31) or GPIO_ENABLE1_REG (GPIOs 32-39). Clear this bit to disable the output driver for the GPIO pin.

2. For an open drain output, set the GPIO_PINx_PAD_DRIVER bit in the GPIO_PINx register corresponding to GPIO pin x. For push/pull mode (default), clear this bit.
   
3. Configure the IO MUX to select the GPIO Matrix. Set the IO_MUX_x__REG register corresponding to GPIO pin x as follows:
   - Set the function field (MCU_SEL) to the IO MUX function corresponding to GPIO X (this is Function 2—numeric value 2—for all pins).

**Footer:**
Espressif Systems
119
ESP32 TRM (Version 5.6)
Submit Documentation Feedback