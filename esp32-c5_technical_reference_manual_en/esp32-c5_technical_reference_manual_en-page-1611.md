

# Chapter 42 Remote Control Peripheral (RMT)

## 42.1 Overview

The Remote Control (RMT) module is designed to transmit and receive infrared remote control signals. A variety of remote control protocols can be encoded/decoded via software based on the RMT module. The RMT module converts pulse codes stored in the module's built-in RAM into output signals, or converts input signals into pulse codes and stores them in RAM. In addition, the RMT module optionally modulates its output signals with a carrier wave, or optionally demodulates and filters its input signals.

The RMT module has four channels, numbered from zero to three. Each channel is able to independently transmit or receive signals.

* Channels 0 ~ 1 (TX channel) are dedicated to transmitting signals;
* Channels 2 ~ 3 (RX channel) are dedicated to receiving signals.

Each TX/RX channel has the same functionality controlled by a dedicated set of registers and is able to independently transmit or receive data. TX channels are indicated by *n* which is used as a placeholder for the channel number, and by *m* for RX channels.

## 42.2 Features

The RMT module has the following features:

* Four channels:
    - TX channels 0 ~ 1
    - RX channels 2 ~ 3
    - Four channels share a 192 x 32-bit RAM
* The transmitter supports:
    - Normal TX mode
    - Wrap TX mode
    - Modulation on TX pulses
    - Continuous TX mode
    - Multiple channels (programmable) transmitting data simultaneously
* The receiver supports:
    - Normal RX mode