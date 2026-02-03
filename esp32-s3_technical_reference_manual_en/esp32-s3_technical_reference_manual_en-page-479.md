**Chapter 6: IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### **6.5.4.2 SDM Configuration**

The configuration of SDM is shown below:

- Route one of SDM outputs to a pin via GPIO matrix, see Section [6.5.2](#).
- Enable the modulator clock by setting `GPIO_FUNCTION_CLK_EN`.
- Configure the divider value by setting `GPIO_SDn_PRESCALE`.
- Configure the duty cycle of SDM output signal by setting `GPIO_SDn_IN`.

---

### **6.6 Direct Input and Output via IO MUX**

#### 6.6.1 Overview

Some high-speed signals (SPI and JTAG) can bypass GPIO matrix for better high-frequency digital performance. In this case, IO MUX is used to connect these pins directly to the peripherals.

This option is less flexible than routing signals via GPIO matrix, as the IO MUX register for each GPIO pin can only select from a limited number of functions, but high-frequency digital performance can be improved.

#### 6.6.2 Functional Description

Two registers must be configured in order to bypass GPIO matrix for peripheral input signals:

1. `IO_MUX_MCU_SEL` - For the GPIO pin must be set to the required pin function. For the list of pin functions, please refer to Section [6.12](#).
2. Clear `GPIO_SIGN_IN_SEL` to route the input directly to the peripheral.

To bypass GPIO matrix for peripheral output signals, `IO_MUX_MCU_SEL` - For the GPIO pin must be set to the required pin function. Please see list of functions in Section 6.12

**Note:**
Not all signals can be connected to peripheral via IO MUX. Some input/output signals can only be connected to peripheral via GPIO matrix.

---

### **6.7 RTC IO MUX for Low Power and Analog Input/Output**

#### 6.7.1 Overview

ESP32-S3 provides 22 GPIO pins with low power capabilities (RTC) and analog functions, which are handled by the RTC subsystem of ESP32-S3. IO MUX and GPIO matrix are not used for these functions; rather, RTC IO MUX is used to redirect 22 RTC input/output signals to the RTC subsystem.

When configured as RTC GPIOs, the output pins can still retain the output level value when the chip is in Deep-sleep mode, and the input pins can wake up the chip from Deep-sleep. 

---

**Espressif Systems**

**479**

**ESP32-S3 TRM (Version 1.7)**

**Submit Documentation Feedback**