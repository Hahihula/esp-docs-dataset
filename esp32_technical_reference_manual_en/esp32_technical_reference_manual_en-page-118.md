**Chapter 6: IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

3. **Configure the IO MUX to select the GPIO Matrix. Set the IO_MUX_ X_ REG register corresponding to GPIO pin X as follows:**

   - Set the function field (MCU_SEL) to the IO MUX function corresponding to GPIO 2—numeric value 2—for all pins.
   
   - Enable the input by setting the FUN_IE bit.

   - Set or clear the FUN_WPU and FUN_WPD bits, as desired, to enable/disable internal pull-up/pull-down resistors.

**Notes:**

- One input pin can be connected to multiple input signals.  
- The input signal can be inverted with GPIO_FUNC Y_ IN_INV_SEL.
- It is possible to have a peripheral read a constantly low or high input value without connecting this input to a pin. This can be done by selecting a special GPIO_FUNC Y_ IN_SEL input, instead of a GPIO number:
  - When GPIO_FUNC Y_ IN_SEL is 0x30, input_signal X is always 0.
  - When GPIO_FUNC Y_ IN_SEL is 0x38, input_signal X is always 1.

For example, to connect RMT peripheral channel 0 input signal (RMT SIG_INO_IDX, signal index 83) to GPIO pin 15, please follow the steps below. Note that GPIO 15 is also named the MTDO pin:
   - Set the GPIO_FUNC83_IN_CFG register field GPIO_FUNC83_IN_SEL value to 15.
   - As this is an input-only signal, set GPIO_FUNC15_OEN_SEL bit in GPIO_FUNC15_OUT_SEL_CFG_REG.
   - Clear bit 15 of GPIO_ENABLE_REG (field GPIO_ENABLE_DATA[15]).
   - Set the IO_MUX_GPIO15 register MCU_SEL field to 2 (GPIO function) and also set the FUN_IE bit (input mode).

---

**6.2.3 Simple GPIO Input**

The GPIO_IN_REG/GPIO_IN1_REG register holds the input values of each GPIO pin.

The input value of any GPIO pin can be read at any time without configuring the GPIO Matrix for a particular peripheral signal. However, it is necessary to enable the input in the IO MUX by setting the FUN_IE bit in the IO_MUX_ X_ REG register corresponding to pin X, as mentioned in Section 6.2.

---

**6.3 Peripheral Output via GPIO Matrix**

**6.3.1 Summary**

To output a signal from a peripheral via the GPIO Matrix, the GPIO Matrix is configured to route the peripheral output signal (0-18, 23-37, 61-121, 140-125, 224-228) to one of the 28 GPIOs (0-19, 21-23, 25-27, 32-33).

The output signal is routed from the peripheral into the GPIO Matrix. It is then routed into the IO MUX, which is configured to set the chosen pin to “GPIO” function. This causes the output GPIO signal to be connected to the pin.

---

**Espressif Systems**

**118**

**ESP32 TRM (Version 5.6)**

**Submit Documentation Feedback**