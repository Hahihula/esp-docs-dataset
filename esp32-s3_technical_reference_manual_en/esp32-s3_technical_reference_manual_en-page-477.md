**Chapter: IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Note:
There is a range of peripheral output signals (208 ~ 212 in Table 6.1-1) which are not connected to any peripheral, but to the input signals (208 ~ 212) directly. These can be used to input a signal from one GPIO pin and output directly to another GPIO pin.

---

#### **6.5.2 Functional Description**

Some of the 256 output signals (signals with a name assigned in the column "Output signal" in Table 6.1-1) can be set to go through GPIO matrix into IO MUX and then to a pin. Figure 6.3-1 illustrates the configuration.

To output peripheral signal Y to a particular GPIO pin X, follow these steps:

1. **Configure GPIO_FUNCx_OUT_SEL_CFG_REG** and **GPIO_ENABLE_REG[x]** corresponding to GPIO pin X in GPIO matrix.
   - Recommended operation: use corresponding WITS (write 1 to set) and WITC (write 1 to clear) registers to set or clear **GPIO ENABLE REG**.

2. Set the **GPIO_FUNCx_OUT_SEL** field in register **GPIO_FUNCx_OUT_SEL_CFG_REG** to the index of the desired peripheral output signal Y.
   - If the signal should always be enabled as an output, set the bit **GPIO_FUNCx_OEN_SEL** in register **GPIO_FUNCx_OUT_SEL_CFG_REG** and the bit in register **GPIO_ENABLE/ENABLE1_WITS_REG**, corresponding to GPIO pin X. To have the output enable signaled by internal logic (for example, the SPIQ\_oe column “Output enable signal when GPIO\_FUNCn\_OEN_SEL = 0” in Table 6.1-1), clear the bit **GPIO_FUNCx_OEN_SEL** instead.

3. Set the corresponding bit in register **GPIO_ENABLE/ENABLE1_WITC_REG** to disable the output from the GPIO pin.
   - For an open drain output, set the bit **GPIO_PINx_PAD_DRIVER** in register **GPIO_PINx_REG** corresponding to GPIO pin X.

4. Configure IO MUX register to enable output via GPIO matrix. Set the **IO_MUX_x_REG** corresponding to GPIO pin X as follows:
   - Set the field **IO_MUX_MGU_SEL** to desired IO MUX function corresponding to GPIO pin X.
     - Function 1 (GPIO function), numeric value 1, for all pins.

5. Set the field **IO_MUXFUN_DRV** to the desired value for output strength (0 ~ 3).
   - If using open drain mode, set/clear **IO_MUXFUN_WPU** and **IO_MUXFUN_WPD** to enable/disable the internal pull-up/pull-down resistors.
     - Note: The output signal from a single peripheral can be sent to multiple pins simultaneously.

6. The output signal can be inverted by setting **GPIO_FUNCx_OUT_INV_SEL**.

---

#### **6.5.3 Simple GPIO Output**

GPIO matrix can also be used for simple GPIO output. This can be done as below:

- Set GPIO matrix **GPIO FUNCn_OUT_SEL** with a special peripheral index 256 (0x100);

---

Espressif Systems  
477  
ESP32-S3 TRM (Version 1.7)  

Submit Documentation Feedback