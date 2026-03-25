

# Chapter 27
## Random Number Generator (RNG)

### 27.1 Introduction

The ESP32-H2 contains a true random number generator, which generates 32-bit random numbers for cryptographic operations and other applications.

### 27.2 Features

The random number generator in ESP32-H2 generates true random numbers, derived from a physical process rather than an algorithm. Each number within the specified range has an equal probability of occurrence.

### 27.3 Functional Description

Every 32-bit value that the system reads from the `LPPERI_RNG_DATA_REG` register of the random number generator is a true random number. These true random numbers are generated based on the **thermal noise** in the system and the **asynchronous clock mismatch**.

- **Thermal noise** comes from the high-speed ADC or SAR ADC or both. Whenever the high-speed ADC or SAR ADC is enabled, bit streams will be generated and fed into the random number generator through an XOR logic gate as random seeds.
- **RC_FAST_CLK** is an asynchronous clock source and it increases the RNG entropy by introducing circuit metastability.

![Figure 27.3-1. Noise Source](image_path)

When there is noise coming from the high-speed ADC, the random number generator is fed with a 2-bit entropy in one APB clock cycle, which is normally 32 MHz.