**Title: Functional Description**

---

### Section Title

#### Subsection (4.1.3.3) Clock  
For details, see [ESP32-C3 Technical Reference Manual](#) > Chapter Reset and Clock.

##### CPU Clock  

The CPU clock has three possible sources:
- external main crystal clock
- fast RC oscillator (typically about 17.5 MHz, and adjustable)
- PLL clock

The application can select the clock source from the three clocks above. The selected clock source drives the CPU clock directly, or after division, depending on the application. Once the CPU is reset, the default clock source would be the external main crystal clock divided by 2.

**Note:**  
ESP32-C3 is unable to operate without an external main crystal clock.

---

##### RTC Clock  

The RTC slow clock is used for RTC counter, RTC watchdog and low-power controller. It has three possible sources:
- external low-speed (32 kHz) crystal clock
- internal slow RC oscillator (typically about 136 kHz, and adjustable)
- internal fast RC oscillator divided clock (derived from the fast RC oscillator or divided by 256)

The RTC fast clock is used for RTC peripherals and sensor controllers. It has two possible sources:
- external main crystal clock divided by 2
- internal fast RC oscillator divide-by-N clock (typically about 17.5 MHz, and adjustable)

---

#### Subsection (4.1.3.4) Interrupt Matrix  

The Interrupt Matrix in the ESP32-C3 chip independently routes peripheral interrupt sources to the ESP-RISC-V CPU’s peripheral interrupts, to timely inform CPU to process the coming interrupts.

##### Feature List  
- Accept 62 peripheral interrupt sources as input
- Generate 31 CPU peripheral interrupts to CPU as output
- Query current interrupt status of peripheral interrupt sources
- Configure priority, type, threshold, and enable signal of CPU interrupts

For details, see [ESP32-C3 Technical Reference Manual](#) > Chapter Interrupt Matrix.

---

**Footer:**  
Espressif Systems  
[Submit Documentation Feedback](#)  
ESP32-C3 Series Datasheet v2.2  

Page 37