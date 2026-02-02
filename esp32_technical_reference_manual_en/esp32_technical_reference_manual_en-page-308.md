**Title:**
Chapter 18

**Subtitle:**
Random Number Generator (RNG)

**Section Title and Content:**

- **18.1 Introduction**
  The ESP32 contains a true random number generator, which generates 32-bit random numbers that can be used for cryptographical operations, among other things.

- **18.2 Feature**
  The random number generator generates true random numbers, which means random number generated from physical process, rather than by means of an algorithm. No number generated within the specified range is more or less likely to appear than any other number.

- **18.3 Functional Description**
  Every 32-bit value that the system reads from the RNG_DATA_REG register of the random number generator is a true random number. These true random numbers are generated based on the thermal noise in the system and the asynchronous clock mismatch.
  
  Thermal noise comes from the high-speed ADC or SAR ADC or both. Whenever the high-speed ADC or SAR ADC is enabled, bit streams will be generated and fed into the random number generator through an XOR logic gate as random seeds.

**Figure Description:**
- **Figure Title:** Figure 18.3-1. Noise Source
- The figure shows a block diagram illustrating how noise from different sources (SAR ADC Random bit seed, High Speed ADC Random bit seed) is fed into the RNG_DATA_REG register through an XOR gate to generate random numbers.

**Additional Information:**
When there is noise coming from the SAR ADC, the random number generator is fed with a 2-bit entropy in one clock cycle of RC_FAST_CLK (8 MHz), which is generated from an internal RC oscillator. It's advisable to read the RNG_DATA_REG register at a maximum rate of 500 kHz to obtain the maximum entropy.

**Footer:**
Espressif Systems
308 ESP32 TRM (Version 5.6)