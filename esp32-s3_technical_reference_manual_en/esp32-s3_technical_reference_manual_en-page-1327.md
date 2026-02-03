**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Diagram Description:**
- The diagram is labeled "Figure 36.2-1. MCPWM Module Overview".
- It shows a block diagram with various components such as "APB BUS", "CLK_160M", "TIMER 0", "TIMER 1", "TIMER 2", and "GPIO MATRIX". There are also labels for "INTERRUPTS" at the top, indicating connections to different timers (SYNC0/SYNC1/SYNC2) which in turn connect to various fault detection mechanisms like "FAULT DETECT" and capture functions.

**Text Content:**

- **Software Features**
  - Software asynchronously overrides control of PWM signals.
  - Configurable dead-time on rising and falling edges; each set up independently.
  - All events can trigger CPU interrupts.
  - Modulating of PWM output by high-frequency carrier signals, useful when gate drivers are insulated with a transformer.

- **Control Registers:**
  - Period, time stamps, and important control registers have shadow registers for flexible updating methods.

**Subsections within the text content include descriptions about specific modules such as:**

1. **Fault Detection Module**
   - Programmable fault handling allocated on fault condition in both cycle-by-cycle mode and one-shot mode.
   - A fault condition can force the PWM output to either high or low logic levels.

2. **Capture Module**
   - Speed measurement of rotating machinery (e.g., toothed spockets sensed with Hall sensors).
   - Measurement of elapsed time between position sensor pulses.
   - Period, duty-cycle measurements derived from pulse train signals for current/voltage decoding and amplitude sensing based on encoded signal patterns or voltage levels.

**Footer:**
- "Espressif Systems"
- Document version information (1327 ESP32-S3 TRM [Version 1.7])
- Links to submit documentation feedback

**Navigation Link:** 
- GoBack