**Title: Functional Description**

ESP32-SOWD (NRND) has a maximum CPU frequency of 160 MHz.

- When Wi-Fi is enabled, the chip switches between Active and Modem-sleep modes. Therefore, power consumption changes accordingly.
- In Modern-sleep mode, the CPU frequency changes automatically. The frequency depends on the CPU load and the peripherals used.
- During Deep-sleep, when the ULP coprocessor is powered on, peripherals such as GPIO and RTC I2C are able to operate.

When the system works in the ULP sensor-monitored pattern, the ULP coprocessor works with the ULP sensor periodically and the ADC works with a duty cycle of 1%, so the power consumption is 100 µA.

**Subtitle: Ultra-Low-Power Coprocessor**

The ULP coprocessor and RTC memory remain powered on during Deep-sleep mode. Hence, the developer can store a program for the ULP coprocessor in the RTC slow memory to access the peripheral devices, internal timers and internal sensors during the deep-sleep mode.

This is useful for designing applications where the CPU needs to be woken up by an external event, or a timer, or a combination of these two, while maintaining minimal power consumption. 

For details, see ESP32 Technical Reference Manual > Chapter ULP Coprocessor.

**Subtitle: Timers and Watchdogs**

**4.4 General Purpose Timers**

There are four general-purpose timers embedded in the chip. They are all 64-bit generic timers which are based on 16-bit prescalers and 64-bit auto-reload-capable up/down-timers.
The timers feature:
- A 16-bit clock prescaler, from 2 to 65536
- A 64-bit timer
- Configurable up/down timer: incrementing or decrementing
- Halt and resume of time-base counter
- Auto-reload at alarming
- Software-controlled instant reload
- Level and edge interrupt generation

For details, see ESP32 Technical Reference Manual > Chapter Timer Group.

**Subtitle: Watchdog Timers**

The chip has three watchdog timers: one in each of the two timer modules (called the Main Watchdog Timer or MWDT) and one in the RTC module (called the RTC Watchdog Timer, or RWDT). These watchdog timers are intended to recover from an unforeseen fault causing the application program to abandon its normal sequence. A watchdog timer has four stages. Each stage may trigger one of three or four possible actions upon the expiry of its programmed time period unless the watchdog is fed or disabled.

**4.4.2 Watchdog Timers**

The chip's description continues with details about each type of watchdog timer, but this text was not provided in full and thus cannot be transcribed here accurately without speculation on content that might exist beyond what has been given.
  
**Footer:**
Espressif Systems
31 ESP32 Series Datasheet v5.2

[Submit Documentation Feedback]