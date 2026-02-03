**Title:**
Chapter 25

**Subtitle:**
Random Number Generator (RNG)

**Section Title and Content:**

- **25.1 Introduction**
  The ESP32-S3 contains a true random number generator, which generates 32-bit random numbers that can be used for cryptographical operations, among other things.

- **25.2 Features**
  The random number generator in ESP32-S3 generates true random numbers, which means random number generated from a physical process, rather than by means of an algorithm. No number generated within the specified range is more or less likely to appear than any other number.

- **25.3 Functional Description**
  Every 32-bit value that the system reads from the RNG_DATA_REG register of the random number generator is a true random number. These true random numbers are generated based on the thermal noise in the system and the asynchronous clock mismatch.
  
  Thermal noise comes from the high-speed ADC or SAR ADC or both. Whenever the high-speed ADC or SAR ADC is enabled, bit streams will be generated and fed into the random number generator through an XOR logic gate as random seeds.

  When the RC_FAST_CLK clock is enabled for the digital core, the random number generator will also sample RC_FAST_CLK (20 MHz) as a random bit seed. RC_FAST_CLK is an asynchronous clock source and it increases the RNG entropy by introducing circuit metastability. However, to ensure maximum entropy, it’s recommended to always enable an ADC source as well.

**Figure:**
- **Figure 25.3-1. Noise Source**

**Diagram Description in Figure (not text but visual):**
The diagram shows a flow from SAR ADC and High Speed ADC feeding into XOR gates which then feed the RNG_DATA_REG register, indicating how random bit seeds are generated through thermal noise.

**Footer:**
When there is noise coming from the SAR ADC, the random number generator is fed with 2-bit entropy in Espressif Systems

**Document Information:**
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback