

# Chapter 32

## Pulse Count Controller (PCNT)

The pulse count controller (PCNT) is designed to count input pulses. It can increment or decrement a pulse counter value by keeping track of rising (positive) or falling (negative) edges of the input pulse signal. The PCNT has four independent pulse counters called units, which have their groups of registers. There is only one clock in PCNT, which is APB_CLK. In this chapter, *n* denotes the number of a unit from 0 ~ 3.

Each unit includes two channels (ch0 and ch1) which can independently increment or decrement its pulse counter value. The remainder of the chapter will mostly focus on channel 0 (ch0) as the functionality of the two channels is identical.

As shown in Figure 32.0-1, each channel has two input signals:

1. One input pulse signal (e.g., `sig_ch0_un`, the input pulse signal for ch0 of unit *n* ch0)
2. One control signal (e.g., `ctrl_ch0_un`, the control signal for ch0 of unit *n* ch0)

![Figure 32.0-1. PCNT Block Diagram](image-placeholder)  
Figure 32.0-1. PCNT Block Diagram

### 32.1 Features

A PCNT has the following features:

* Four independent pulse counters (units) that count from 1 to 65535
* Each unit consists of two independent channels sharing one pulse counter
* All channels have input pulse signals (e.g., `sig_ch0_un`) with their corresponding control signals (e.g., `ctrl_ch0_un`)

Espressif Systems  
936  
ESP32-H2 TRM (Version 1.1)