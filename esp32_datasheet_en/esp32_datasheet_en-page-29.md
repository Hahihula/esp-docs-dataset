**Title: Functional Description**

---

**Table of Cache Addresses and Sizes**
| Category | Target                   | Start Address       | End Address      | Size |
|----------|-------------------------|--------------------|------------------|------|
| Peripheral | SYSCON                  | 0x3FF6_6000        | 0x3FF6_6FFF      | 4 KB |
|          | I2C1                    | 0x3FF6_7000        | 0x3FF6_7FFF      | 4 KB |
|          | SDMMC                   | 0x3FF6_8000        | 0x3FF6_8FFF      | 4 KB |
|          | EMAC                    | 0x3FF6_9000        | 0x3FF6_AFFF      | 8 KB |
|          | TWAI                    | 0x3FF6_B000        | 0x3FF6_BFFF      | 4 KB |
|          | PWM1                    | 0x3FF6_C000        | 0x3FF6_CFFF      | 4 KB |
|          | I2S1                    | 0x3FF6_D000        | 0x3FF6_DFFF      | 4 KB |
|          | UART2                   | 0x3FF6_E000        | 0x3FF6_EFFF      | 4 KB |
|          | PWM2                    | 0x3FF6_F000        | 0x3FF6_FFFF      | 4 KB |
|          | PWM3                    | 0x3FF7_0000        | 0x3FF7_0FFF      | 4 KB |
|          | RNG                     | 0x3FF7_5000        | 0x3FF7_5FFF      | 4 KB |

---

**Subtitle: Cache**

ESP32 uses a two-way set-associative cache. Each of the two CPUs has 32 KB of cache featuring a block size of 32 bytes for accessing external storage.

For details, see [ESP32 Technical Reference Manual](#) > Chapter System and Memory > Section Cache.

---

**Subtitle: System Clocks**

4.2

**Sub-subtitle: CPU Clock (4.2.1)**

Upon reset, an external crystal clock source is selected as the default CPU clock. The external crystal clock source also connects to a PLL to generate a high-frequency clock (typically 160 MHz).

In addition, ESP32 has an internal 8 MHz oscillator. The application can select the clock source from the external crystal clock source, the PLL clock or the internal 8 MHz oscillator. The selected clock source drives the CPU clock directly, or after division, depending on the application.

**Sub-subtitle: RTC Clock (4.2.2)**

The RTC clock has five possible sources:

- External low-speed (32 kHz) crystal clock
- External crystal clock divided by 4
- Internal RC oscillator (typically about 150 kHz, and adjustable)
- Internal 8 MHz oscillator
- Internal 31.25 kHz clock (derived from the internal 8 MHz oscillator divided by 256)

When the chip is in the normal power mode and needs faster CPU accessing, the application can choose the external high-speed crystal clock divided by 4 or the internal 8 MHz oscillator. When the chip operates in low-power mode, the application chooses the external low-speed (32 kHz) crystal clock, the internal RC clock or the internal 31.25 kHz clock.

---

**Footer:**
Espressif Systems  
[Submit Documentation Feedback](#) ESP32 Series Datasheet v5.2

---