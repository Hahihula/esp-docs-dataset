

```markdown
## APB_CLK

The frequency of APB_CLK is determined by the clock source of CPU_CLK as shown in Table 6.2-4.

Table 6.2-4. APB_CLK Clock Frequency

| CPU_CLK Source | APB_CLK Frequency |
|----------------|-------------------|
| PLL_CLK        | 80 MHz            |
| XTAL_CLK       | CPU_CLK           |
| RC_FAST_CLK    | CPU_CLK           |

## CRYPTO_CLK

The frequency of CRYPTO_CLK is determined by the CPU_CLK source, as shown in Table 6.2-5.

Table 6.2-5. CRYPTO_CLK Frequency

| CPU_CLK Source | CRYPTO_CLK Frequency |
|----------------|----------------------|
| PLL_CLK        | 160 MHz              |
| XTAL_CLK       | CPU_CLK              |
| RC_FAST_CLK    | CPU_CLK              |

## PLL_F160M_CLK

PLL_F160M_CLK is divided from PLL_CLK according to current PLL frequency.

## LEDC_SCLK

LEDC module uses RC_FAST_CLK as clock source when APB_CLK is disabled. In other words, when the system is in low-power mode, most peripherals will be halted (as APB_CLK is turned off), but LEDC can still work normally via RC_FAST_CLK.

### 6.2.4.3 Wi-Fi and Bluetooth LE Clock

Wi-Fi and Bluetooth LE can only work when CPU_CLK uses PLL_CLK as its clock source. Suspending PLL_CLK requires that Wi-Fi and Bluetooth LE have entered low-power mode first.

LOW_POWER_CLK uses XTAL32K_CLK, XTAL_CLK, RC_FAST_CLK or RTC_SLOW_CLK (the low clock selected by RTC) as its clock source for Wi-Fi and Bluetooth LE in low-power mode.

### 6.2.4.4 RTC Clock

The clock sources for RTC_SLOW_CLK and RTC_FAST_CLK are low-frequency clocks. RTC module can operate when most other clocks are stopped. RTC_SLOW_CLK derived from RC_SLOW_CLK, XTAL32K_CLK or RC_FAST_DIV_CLK is used to clock Power Management module. RTC_FAST_CLK is used to clock On-chip Sensor module. It can be sourced from a divided XTAL_CLK or from a divided RC_FAST_CLK.
```