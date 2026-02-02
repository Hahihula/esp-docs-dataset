**Chapter Title:**
Chapter 18 Random Number Generator (RNG)

**Body Text:**
When there is noise coming from the high-speed ADC, the random number generator is fed with a 2-bit entropy in one APB clock cycle, which is normally 80 MHz. Thus, it is advisable to read the `RNG_DATA_REG` register at a maximum rate of 5 MHz to obtain the maximum entropy.

A data sample of 2 GB, which is read from the random number generator at a rate of 5 MHz with only the high-speed ADC being enabled, has been tested using the Dieharder Random Number Testsuite (version 3.31.1). The sample passed all tests.

**Subheading:**
18.4 Programming Procedure

**Body Text:**
When using the random number generator, make sure at least either the SAR ADC or high-speed ADC is enabled. Otherwise, pseudo-random numbers will be returned.
- SAR ADC can be enabled by using the DIG ADC controller. For details, please refer to Chapter 31 On-Chip Sensors and Analog Signal Processing.

**Bullet Points:**
- High-speed ADC is enabled automatically when the Wi-Fi or Bluetooth modules is enabled.

**Note Section:**
Note:
- Note that, when the Wi-Fi module is enabled, the value read from the high-speed ADC can be saturated in some extreme cases, which lowers the entropy. Thus, it is advisable to also enable the SAR ADC as the noise source for the random number generator for such cases.
When using the random number generator, read the `RNG_DATA_REG` register multiple times until sufficient random numbers have been generated. Ensure the rate at which the register is read does not exceed the frequencies described in section 18.3 above.

**Subheading:**
18.5 Register Summary

**Table:**
| Name          | Description                   | Address       | Access |
|---------------|-------------------------------|--------------|--------|
| RNG_DATA_REG  | Random number data            | 0x3FF75144   | RO     |

**Subheading:**
18.6 Register

**Body Text:**
Register 18.1. `RNG_DATA_REG` (0x3FF75144)

**Diagram Description:**
- Diagram showing the address and access information for `RNG_DATA_REG`.

**Footer Information:**
Espressif Systems
Page number: 309
ESP32 TRM (Version 5.6)
Submit Documentation Feedback