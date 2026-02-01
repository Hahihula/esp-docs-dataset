Title: Functional Description

- Active mode – The HP CPU, RF circuits, and all peripherals are on. The chip can process data, receive, transmit, and listen.
  
- Modem-sleep mode – The HP CPU is on, but the clock frequency can be reduced. The wireless connections can be configured to remain active as RF circuits are periodically switched on when required.

- Light-sleep mode – The HP CPU stops running, and can be optionally powered on. The LP peripherals, as well as the LP CPU can be woken up periodically by the timer. The chip can be woken up via all wake up mechanisms: MAC, RTC timer, or external interrupts. Wireless connections can remain active. Some groups of digital peripherals can be optionally powered off.

- Deep-sleep mode – Only the LP system is powered on. Wireless connection data is stored in LP memory.
  
For details, see [ESP32-C5 Technical Reference Manual](#) > Chapter Low-Power Management.

Subtitle: 4.1.3.7 System Timer

Body Text:
The System Timer (SYSTIMER) in the ESP32-C5 chip is a 52-bit timer that can be used to generate tick interrupts for the operating system or as a general timer to generate periodic or one-time interrupts.

Subtitle: Feature List
- two 52-bit counters and three 52-bit comparators
- counters with an average clock frequency of 16 MHz
- three types of independent interrupts generated according to alarm value
- two alarm modes: target mode and period mode
- 52-bit alarm values and 26-bit alarm periods
- automatic reload of counter value
- counters can be stalled if the CPU is stalled or in OCD mode
- real-time alarm events

For details, see [ESP32-C5 Technical Reference Manual](#) > Chapter System Timer.

Subtitle: 4.1.3.8 Timer Group

Body Text:
The Timer Group (TIMG) in the ESP32-C5 chip can be used to precisely time an interval, trigger an interrupt after a particular interval (periodically and aperiodically), or act as a hardware clock. ESP32-C5 has two timer groups, TIMGO and TIMG1, each consisting of one general-purpose timer and one Main System Watchdog Timer.

Subtitle: Feature List
- 16-bit prescaler
- 54-bit time-base counter programmable to incrementing or decrementing
- able to read real-time value of the time-base counter
- halt and resume the time-base counter

Footer:
Espressif Systems  
[Submit Documentation Feedback](#)  
ESP32-C5 Series Datasheet v1.0