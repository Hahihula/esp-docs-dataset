

```markdown
- Figure 5.3-2 shows in details how IO MUX and GPIO matrix route signals from pins to peripherals, and from peripherals to pins.
- Figure 5.3-3 shows the interface logic for a GPIO pin.

Figure 5.3-1. Diagram of IO MUX and GPIO Matrix

Peripherals
• SPI
• RMT
• I2S
• TWAI
• ...
In total:
42 peripheral inputs
78 peripheral outputs

GPIO Matrix → IO MUX → PIN (GPIO6~21)
PIN (GPIO0~5)

VDD3P3_CPU Power Domain
VDD3P3_RTC Power Domain

Figure 5.3-2. Architecture of IO MUX and GPIO Matrix

① Only part of peripheral input signals (marked “yes” in column “Direct input through IO MUX” in Table 5.11-1) can bypass GPIO matrix. The other input signals can only be routed to peripherals via GPIO matrix.
② There are only 22 inputs from GPIO SYNC to GPIO matrix, since ESP32-C3 provides 22 GPIO pins in
```