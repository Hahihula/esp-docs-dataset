**Title:**
Chapter 2

**Subtitle:**
ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Section Title:**
2.1 Overview

**Body Text:**
The ULP coprocessor is an ultra-low-power processor that remains powered on when the chip is in Deep-sleep (see Chapter 10 Low-power Management [RTC_CNTL]). Hence, users can store in RTC memory a program for the ULP coprocessor to access RTC peripherals, internal sensors, and RTC registers during Deep-sleep.

In power-sensitive scenarios, the main CPU goes to sleep mode to lower power consumption. Meanwhile, the coprocessor is woken up by ULP timer, and then monitors the external environment or interacts with the external circuit by controlling peripherals such as RTC GPIO, RTC I2C, SAR ADC, or temperature sensor (TSENS). The coprocessor wakes the main CPU up once a wakeup condition is reached.

**Image Description:**
Figure 2.1-1 shows an overview of ULP Coprocessor Overview with labels indicating "Enable by ULP or Main CPU," "ULP Timer" connected to "RTC GPIO," and other components like "ULP Coprocessor (RTC_CNTL)," "ADC," "TSENS." The diagram also includes connections labeled as "Wakeup."

**Additional Information:**
ESP32-S3 has two ULP coprocessors, with one based on RISC-V instruction set architecture (ULP-RISC-V) and the other on finite state machine (ULP-FSM). Users can choose between the two coprocessors depending on their needs.

**Section Title:**
2.2 Features

**List of Features:**
- Access up to 8 KB of SRAM RTC slow memory for instructions and data
- Clocked with 17.5 MHz RTC_FAST_CLK

**Footer Information:**
Espressif Systems  
304 ESP32-S3 TRM (Version 1.7)  
[Submit Documentation Feedback](#)