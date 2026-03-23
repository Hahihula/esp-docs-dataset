

# Chapter 26

## Random Number Generator (RNG)

### 26.1 Introduction

The ESP32-C6 contains a true random number generator, which generates 32-bit random numbers that can be used for cryptographical operations, among other things.

### 26.2 Features

The random number generator in ESP32-C6 generates true random numbers, which means random numbers generated from a physical process, rather than by means of an algorithm. No number generated within the specified range is more or less likely to appear than any other number.

### 26.3 Functional Description

Every 32-bit value that the system reads from the `LPPERI_RNG_DATA_REG` register of the random number generator is a true random number. These true random numbers are generated based on the **thermal noise** in the system and the **asynchronous clock mismatch**.

- **Thermal noise** comes from the high-speed ADC or SAR ADC or both. Whenever the high-speed ADC or SAR ADC is enabled, bit streams will be generated and fed into the random number generator through an XOR logic gate as random seeds.
- **RC_FAST_CLK** is an asynchronous clock source and it increases the RNG entropy by introducing circuit metastability.

![Figure 26.3-1. Noise Source](image_path_if_visible)

When there is noise coming from the SAR ADC, the random number generator is fed with a 2-bit entropy in one clock cycle of RC_FAST_CLK, which is generated from an internal RC oscillator (see Chapter 8 *Reset and*).