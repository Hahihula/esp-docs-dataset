

# Chapter 48

## Pulse Count Controller (PCNT)

The pulse count controller (PCNT) is designed to count input pulses.

### 48.1 Introduction

Figure 48.1-1. PCNT Overview

As shown in Figure 48.1-1, PCNT has four independent pulse counters called units, which have their groups of registers. Each unit includes two channels (ch0 and ch1) and a 16-bit signed counter. Each channel has an input pulse signal and an input signal filtering module. The 16-bit signed counter can be configured for incremental or decremental counting. The clock for PCNT module is APB_CLK.

### 48.2 Feature List

A PCNT has the following features:

* Four independent pulse counters (units) that count from 1 to 65535
* Each unit consists of two independent channels sharing one pulse counter
* All channels have input pulse signals (e.g., sig_ch0_un) with their corresponding control signals (e.g., ctrl_ch0_un)
* Independently filter glitches of input pulse signals (sig_ch0_un and sig_ch1_un) and control signals (ctrl_ch0_un and ctrl_ch1_un) on each unit