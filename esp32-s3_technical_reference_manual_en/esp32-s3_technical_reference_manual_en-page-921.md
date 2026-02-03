**Title: Chapter 25 Random Number Generator (RNG)**

---

**Body Text:**

one clock cycle of RC_FAST_CLK (20 MHz), which is generated from an internal RC oscillator (see Chapter 7 Reset and Clock for details). Thus, it is advisable to read the RNG_DATA_REG register at a maximum rate of 500 kHz to obtain the maximum entropy.

When there is noise coming from the high-speed ADC, the random number generator is fed with a 2-bit entropy in one APB clock cycle, which is normally 80 MHz. Thus, it is advisable to read the RNG_DATA_REG register at a maximum rate of 5 MHz to obtain the maximum entropy.

---

**Subtitle: 25.4 Programming Procedure**

When using the random number generator, make sure at least either the SAR ADC, high-speed ADC, or RC_FAST_CLK is enabled. Otherwise, pseudo-random numbers will be returned.
- SAR ADC can be enabled by using the DIG ADC controller. For details, please refer to Chapter 39 On-Chip Sensors and Analog Signal Processing.

High-speed ADC is enabled automatically when the Wi-Fi or Bluetooth modules is enabled.

RC_FAST_CLK is enabled by setting the RTC_CNTL_DIG_CLK8M_EN bit in the RTC_CNTL_CLK_CONF_REG register.

**Note:**
Note that, when the Wi-Fi module is enabled, the value read from the high-speed ADC can be saturated in some extreme cases, which lowers the entropy. Thus, it is advisable to also enable the SAR ADC as the noise source for the random number generator for such cases.

When using the random number generator, read the RNG_DATA_REG register multiple times until sufficient random numbers have been generated. Ensure the rate at which the register is read does not exceed the frequencies described in section 25.3 above.

---

**Subtitle: 25.5 Register Summary**

The abbreviations given in Column Access are explained in Section Access Types for Registers.
| Name | Description | Address | Access |
|------|-------------|---------|--------|
| RNG_DATA_REG | Random number data | 0x6003_507C | RO |

---

**Footer:**
Espressif Systems  
921  
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)