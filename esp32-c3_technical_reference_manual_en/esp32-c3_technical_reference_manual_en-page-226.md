

```markdown
default, and outputs high level when the voltage of the detected pin drops below the predefined threshold.

RTC_CNTL_BROWN_OUT_RST_SEL configures the reset type. For more information regarding chip reset and system reset, please refer to 6 Reset and Clock.

*   0: resets the chip
*   1: resets the system

The brownout detector has ultra-low power consumption and remains enabled whenever the chip is powered up. For the architecture of the ESP32-C3 brownout detector, see Figure 9.3-7.

Figure 9.3-7. Brown-out detector

## 9.4 Power Modes Management

### 9.4.1 Power Domain

ESP32-C3 has 9 power domains in three power domain categories:

*   **RTC**
    *   Power management unit (PMU), including RTC timer, fast memory, Always-on registers
*   **Digital**
    *   PD peripherals, including SPI2, GDMA, SHA, RSA, AES, HMAC, DS, Secure Boot
    *   Digital system
    *   Wireless digital circuits
    *   CPU
*   **Analog**
    *   RC_FAST_CLK
    *   XTAL_CLK
    *   PLL
    *   RF circuits
```