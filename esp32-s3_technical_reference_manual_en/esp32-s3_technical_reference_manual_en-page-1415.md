**Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Subtitle:**
Remote Control Peripheral (RMT)

**Section Title:**
37.1 Overview

**Body Text:**
The RMT module is designed to send and receive infrared remote control signals. A variety of remote control protocols can be encoded/decoded via software based on the RMT module. The RMT module converts pulse codes stored in the module’s built-in RAM into output signals, or converts input signals into pulse codes and stores them in RAM. In addition, the RMT module optionally modulates its output signals with a carrier wave, or optionally demodulates and filters its input signals.

The RMT module has eight channels, numbered from zero to seven. Each channel is able to independently transmit or receive signals.
- Channel 0 ~ 3 (TX channel) are dedicated to sending signals.
- Channel 4 ~ 7 (RX channel) are dedicated to receiving signals.

Each TX/RX channel is controlled by a dedicated set of registers with the same functionality. Channel 3 and channel 7 support DMA access, so the two channels also have a set of DMA-related control and status registers. Registers for each TX channel are indicated by `n` which is used as a placeholder for the channel number, and `m` for each RX channel.

**Section Title:**
37.2 Features

**List:**
- Four TX channels
- Four RX channels
- Support multiple channels (programmable) transmitting data simultaneously
- Eight channels share a 384 x 32-bit RAM
- Support modulation on TX pulses
- Support filtering and demodulation on RX pulses
- Wrap TX mode
- Wrap RX mode
- Continuous TX mode
- DMA access for TX mode on channel 3
- DMA access for RX mode on channel 7

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
ESP32-S3 TRM (Version 1.7)