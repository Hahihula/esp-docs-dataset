

```markdown
Chapter 30

I2S Controller (I2S)

30.1 Overview

ESP32-C6 has a built-in I2S interface, which provides a flexible communication interface for streaming digital data in multimedia applications, especially digital audio applications.

The I2S standard bus defines three signals: a bit clock signal (BCK), a channel/word select signal (WS), and a serial data signal (SD). A basic I2S data bus has one master and one slave. The roles remain unchanged throughout the communication. The I2S module on ESP32-C6 provides separate transmit (TX) and receive (RX) units for high performance.

30.2 Terminology

To better illustrate the functionality of I2S, the following terms are used in this chapter.

Master mode        As a master, I2S drives BCK/WS signals, and sends data to or receives data from a slave.
Slave mode          As a slave, I2S is driven by BCK/WS signals, and receives data from or sends data to a master.
Full-duplex         There are two separate data lines. Transmitted and received data are carried simultaneously.
Half-duplex         Only one side, the master or the slave, sends data first, and the other side receives data. Sending data and receiving data can not happen at the same time.

A-law and μ-law     A-law and μ-law are compression/decompression algorithms in digital pulse code modulated (PCM) non-uniform quantization, which can effectively improve the signal-to-quantization noise ratio.

TDM RX mode         In this mode, pulse code modulated (PCM) data is received and stored into memory via direct memory access (DMA), utilizing time division multiplexing (TDM). The signal lines include: BCK, WS, and SD. Data from 16 channels at most can be received. TDM Philips standard, TDM MSB alignment standard, and TDM PCM standard are supported in this mode, depending on user configuration.

Normal PDM RX mode   In this mode, pulse density modulation (PDM) data is received and stored into memory via DMA. Used signals: WS and DATA. PDM standard is supported in this mode by user configuration.
```