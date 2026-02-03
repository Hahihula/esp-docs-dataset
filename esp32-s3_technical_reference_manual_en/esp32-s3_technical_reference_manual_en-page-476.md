**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Section Titles with Subsections:**

1. **4. Configure IO MUX register to enable pin input. For this end, please set IO_MUX_X_REG corresponding to GPIO pin x as follows:**
   - Set IO_MUXFUN_ICE to enable input².
   - Set or clear IO_MUXFUN_WPU and IO_MUXFUN_WPD, as desired, to enable or disable pull-up and pull-down resistors.

2. **For example, to connect RMT channel 0 input signal³ (rmt_sig_in0, signal index 81) to GPIO40, please follow the steps below. Note that GPIO40 is also named as MTDIO pin:**
   - Set GPIO SIG81_IN_SEL in register GPIO_FUNC81_IN_SEL_CFG_REG to enable peripheral signal input via GPIO matrix.
   - Set GPIO_FUNC81_IN_SEL in register GPIO_FUNC81_IN_SEL_CFG_REG to 40, i.e., select GPIO40.

3. **Set IO_MUXFUN_ICE in register IO_MUX_GPIO40_REG to enable pin input.**

**Note:**
- One pin input can be connected to multiple peripheral input signals.
- The input signal can be inverted by configuring GPIO_FUNCy_IN_INV_SEL.
- It is possible to have a peripheral read a constantly low or constantly high input value without connecting this input to a pin.

  - When GPIO_FUNCy_IN_SEL is set to 0x3C, input signal is always 0.
  - When GPIO_FUNCy_IN_SEL is set to 0x38, input signal is always 1.

**Subsection Titles and Content:**

- **6.4.4 Simple GPIO Input**
  - GPIO_IN_REG/GPIO_IN1_REG holds the input values of each GPIO pin. The input value of any GPIO pin can be read at any time without configuring GPIO matrix for a particular peripheral signal. However, it is necessary to enable pin input by setting IO_MUXFUN_ICE in register IO_MUX_X_REG corresponding to pin X, as described in Section 6.4².

- **6.5 Peripheral Output via GPIO Matrix**
  - **6.5.1 Overview**

    To output a signal from a peripheral via GPIO matrix, the matrix is configured to route peripheral output signals (only signals with a name assigned in the column "Output signal" in Table 6.11) to one of the 45 GPIOs (0 ~ 21, 26 ~ 48).

    The output signal is routed from the peripheral into GPIO matrix and then into IO MUX. IO MUX must be configured to set the chosen pin to GPIO function. This enables the output GPIO signal to be connected to the pin.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Page Number:** 
476