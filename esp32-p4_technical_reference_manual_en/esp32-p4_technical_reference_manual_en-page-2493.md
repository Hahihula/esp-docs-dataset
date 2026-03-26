

# Chapter 47

## LP I2S Controller

### 47.1 Introduction

ESP32-P4 has a built-in LP I2S interface, which provides a data reception communication interface for **Voice Activity Detection (VAD)** and some digital audio applications in low power mode.

The I2S standard bus defines three signals, namely, a bit clock signal (BCK), a channel/word select signal (WS), and a serial data signal (SD). A basic I2S data bus has one master and one slave. The roles remain unchanged throughout the communication.

The LP I2S module on ESP32-P4 provides an independent RX unit, which supports receiving data when the chip is running with the lowest power consumption. Compared to HP I2S, i.e., **I2S0**, **I2S1**, and **I2S2**, LP I2S does not support DMA access. Instead, it uses a separate internal memory to store data.

**Note:**
For I2S-related terminology, refer to the Section 46.2 Terminology in Chapter 46 I2S Controller (I2S).

### 47.2 Feature List

The LP I2S module has the following features:

- RX master mode and slave mode
- A variety of audio standards supported:
    - TDM Philips standard
    - TDM MSB alignment standard
    - TDM PCM standard
    - PDM standard
- Various RX modes supported:
    - TDM RX mode, up to 2 channels supported
    - PDM RX mode

    * Raw PDM data reception
    * PDM-to-PCM data format conversion, up to 2 channels supported

- Configurable sample clock with a variety of sampling frequencies supported
- 16-bit data communication