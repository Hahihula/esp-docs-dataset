**Title: Functional Description**

---

### **4.1.3.3 Clock**

#### CPU Clock

The CPU clock has three possible sources:

- External main crystal clock
- Internal fast RC oscillator (typically about 17.5 MHz, adjustable)
- PLL clock

The application can select the clock source from the three clocks above. The selected clock source drives the CPU clock directly, or after division, depending on the application. Once the CPU is reset, the default clock source would be the external main crystal clock divided by 2.

**Note:** ESP32-S3 is unable to operate without an external main crystal clock.

#### RTC Clock

The RTC slow clock is used for RTC counter, RTC watchdog and low-power controller. It has three possible sources:

- External low-speed (32 kHz) crystal clock
- Internal slow RC oscillator (typically about 136 kHz, adjustable)
- Internal fast RC oscillator divided clock (derived from the internal fast RC oscillator divided by 256)

The RTC fast clock is used for RTC peripherals and sensor controllers. It has two possible sources:

- External main crystal clock divided by 2
- Internal fast RC oscillator (typically about 17.5 MHz, adjustable)

For details, see ESP32-S3 Technical Reference Manual > Chapter Reset and Clock.

---

### **4.1.3.4 Interrupt Matrix**

The interrupt matrix embedded in ESP32-S3 independently allocates peripheral interrupt sources to the two CPUs’ peripheral interrupts, to timely inform CPU0 or CPU1 to process the interrupts once the interrupt signals are generated.

#### Feature List

- 99 peripheral interrupt sources as input
- Generate 26 peripheral interrupts to CPU0 and 26 peripheral interrupts to CPU1 as output.
  Note that the remaining six CPU0 interrupts and six CPU1 interrupts are internal interrupts.
- Disable CPU non-maskable interrupt (NMI) sources
- Query current interrupt status of peripheral interrupt sources

For details, see ESP32-S3 Technical Reference Manual > Chapter Interrupt Matrix.

---

**Footer:**
Espressif Systems  
42  
Submit Documentation Feedback  
ESP32-S3 Series Datasheet v2.1