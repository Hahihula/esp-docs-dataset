**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Body Text:**

- **Power isolation unit:** isolates different power domains, so powered up and powered down domains do not affect each other.

- **Low-power clocks:** provide clocks to power domains working in low-power modes.
  
- **Timers:**
  - RTC timer: logs the status of the RTC main state machine in dedicated registers.
  - ULP timer: wakes up the ULP co-processors at a predefined time. For details, please refer to Chapter [2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)](https://example.com).
  - Touch sensor timer: wakes up the touch sensor at a predefined time. For details, please refer to Chapter [39 On-Chip Sensors and Analog Signal Processing](https://example.com).

- **8 x 32-bit “always-on” retention registers:** These registers are always powered up and are not affected by any low-power modes; thus can be used for storing data that cannot be lost.

- **22 x “always-on” pins:** These pins are always powered up and do not affect the power domains. They may serve as wake-up sources when in a low-power mode (for details, please refer to Section [10.4.4](https://example.com)), or can function like regular GPIOs for more information see Chapter 6 on I/O MUX and GPIO Matrix ([GPIO, IO MUX](https://example.com)).

- **RTC slow memory:** 8 KB SRAM that operates under RTC fast clock (rtc_fast_clk), which may be used as extended memory to store ULP co-processor directives and data.
  
- **RTC fast memory:** 8 KB SRAM operating at CPU clock speed (CPU_CLK), potentially serving an expanded role in the system.

- **Voltage regulators:** regulate power supply for different domains of operation. 

**Additional Information:**
The schematic diagram illustrating ESP32-S3’s low-power management is shown as Figure [10.3-1](https://example.com).

**Footer Text:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback