

# Chapter 57
## Remote Control Peripheral (RMT)

### 57.1 Overview

The Remote Control (RMT) module is designed to transmit and receive infrared remote control signals. A variety of remote control protocols can be encoded/decoded via software based on the RMT module. The RMT module converts pulse codes stored in the module's built-in RAM into output signals, or converts input signals into pulse codes and stores them in RAM. In addition, the RMT module optionally modulates its output signals with a carrier wave, or optionally demodulates and filters its input signals.

The RMT module has eight channels, numbered from zero to seven. Each channel is able to independently transmit or receive signals.

* Channel 0 ~ 3 (TX channel) are dedicated to transmitting signals;
* Channel 4 ~ 7 (RX channel) are dedicated to receiving signals.

Each TX/RX channel has the same functionality controlled by a dedicated set of registers and is able to independently transmit or receive data. Channel 3 and channel 7 support GDMA access, so the two channels also have a set of GDMA-related control and status registers. TX channels are indicated by *n* which is used as a placeholder for the channel number, and by *m* for RX channels.

### 57.2 Features

The RMT module has the following features:

* Eight channels:
    - TX channels 0 ~ 3
    - RX channels 4 ~ 7
    - Eight channels share a 384 x 32-bit RAM
* The transmitter supports:
    - Normal TX mode
    - Wrap TX mode
    - Continuous TX mode
    - Modulation on TX pulses
    - Multiple channels transmitting data simultaneously (programmable)
    - GDMA access supported by TX channel 3