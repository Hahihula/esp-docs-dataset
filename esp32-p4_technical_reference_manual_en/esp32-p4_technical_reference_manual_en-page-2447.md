

```markdown
Chapter 46 I2S Controller (I2S)
GoBack

Chapter 46

I2S Controller (I2S)

46.1 Overview

ESP32-P4 has three built-in I2S interfaces (i.e., I2S0, I2S1, and I2S2), which provide flexible communication interfaces for streaming digital data in multimedia applications, especially digital audio applications.

The I2S standard bus defines three signals, namely, a bit clock signal (BCK), a channel/word select signal (WS), and a serial data signal (SD). A basic I2S data bus has one master and one slave. The roles remain unchanged throughout the communication. The I2S module on ESP32-P4 provides separate transmit (TX) and receive (RX) units for high performance.

Note:
The information provided in this chapter applies to I2S0, I2S1, and I2S2. Unless otherwise indicated, I2S or I2Sn in this chapter refer to I2S0, I2S1, and I2S2.

46.2 Terminology

To better illustrate the functionality of I2S, the following terms are used in this chapter.

Master mode        As a master, I2Sn drives BCK/WS signals and transmits data to or receives data from a slave.
Slave mode          As a slave, I2Sn is driven by BCK/WS signals and receives data from or transmits data to a master.
Full-duplex         There are two separate data lines. The transmitted and received data is carried simultaneously.
Half-duplex         Only one side, the master or the slave, transmits data first, and the other side receives data. Data transmission and reception cannot occur simultaneously.
A-law and μ-law     A-law and μ-law are compression/decompression algorithms in digital pulse code modulated (PCM) non-uniform quantization, which can effectively improve the signal-to-quantization noise ratio.
TDM RX mode         In this mode, pulse code modulated (PCM) data is received utilizing time division multiplexing (TDM). The signal lines include BCK, WS, and SD. Data from 16 channels at most can be received. TDM Philips standard, TDM MSB alignment standard, and TDM PCM standard are supported in this mode, depending on user configuration.
```