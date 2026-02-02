**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Body Text with List and Subsections:**

5. When the power-domain digital core is powered down, all included in power domains are powered down.

6. The power-domain Wi-Fi includes the Wi-Fi MAC and BB.
7. Each internal SRAM can be power-gated independently.

---

**Subtitle:** 9.3.9 Predefined Power Modes

In ESP32, we recommend that you always use the predefined power modes first, before trying to tune each power control signal. The predefined power modes should cover most scenarios:

- **Active mode**
  - The CPU is clocked at XTAL_DIV_N (40 MHz/26 MHz) or PLL (80 MHz/160 MHz/240 MHz).
  - The chip can receive, transmit, or listen.

- **Modem-sleep mode**
  - The CPU is operational and the clock is configurable.
  - The Wi-Fi/Bluetooth baseband is clock-gated or powered down. The radio is turned off.
    - Current consumption: ~30 mA with 80 MHz PLL.
    - Current consumption: ~3 mA with 2 MHz XTAL.

- **Immediate wake-up**

- **Light-sleep mode**
  - The internal 8 MHz oscillator, 40 MHz high-speed crystal, PLL, and radio are disabled.
  - The clock in the digital core is gated. The CPUs are stalled.
  - The ULP coprocessor and touch controller can be periodically triggered by monitor sensors.
    - Current consumption: ~ 800 µA.

- **Wake-up latency:** less than 1 ms.

- **Deep-sleep mode**
  - The internal 8 MHz oscillator, 40 MHz high-speed crystal, PLL and radio are disabled.
  - The digital core is powered down. The CPU context is lost.
  - The supply voltage to the RTC core drops to 0.7V.
    - 8 x 32 bits of data are kept in general-purpose retention registers.

- **The RTC memory and fast RTC memory can be retained.**
  - Current consumption: ~ 6.5 µA.

- **Wake-up latency:** less than 1 ms.

- Recommended for ultra-low-power infrequently-connected Wi-Fi/Bluetooth applications.

- **Hibernatation mode**
  - The internal 8 MHz oscillator, 40 MHz high-speed crystal, PLL, and radio are disabled.
  - The digital core is powered down. The CPU context is lost.

**Footer:**
Espressif Systems
189 ESP32 TRM (Version 5.6)
[Submit Documentation Feedback](#)