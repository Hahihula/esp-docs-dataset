

# Chapter 41

## Voice Activity Detection (VAD)

### 41.1 Introduction

ESP32-P4 integrates a Voice Activity Detection (VAD) module. This module facilitates the hardware implementation of the first-stage algorithm for voice wake-up and other multimedia functions. Additionally, it provides hardware support for low-power voice wake-up solutions.

### 41.2 Feature List

The VAD module has the following features:

- VAD algorithm processes voice data frame by frame, with each frame containing 256 data points. The data sampling rate is 8 kHz, and the bit width is 16 bits
- 2 KB buffer that stores up to 4 frames of data
- Independent system wake-up source
- Configurable interrupt sources
- Flexible configuration of algorithm parameters

### 41.3 Architectural Overview

Figure 41.3-1 is the block diagram of the ESP32-P4 VAD module. The VAD module includes:

- Energy threshold check
- FFT (Fast Fourier Transform) calculation
- LTSD (Long-Term Spectral Divergence) calculation