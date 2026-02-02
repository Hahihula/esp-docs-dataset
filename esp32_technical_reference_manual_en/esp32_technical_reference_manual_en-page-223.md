**Chapter Title:**
Chapter 10 Timer Group (TIMG)

**GoBack Link:** [GoBack](#)

---

### 10.1 Introduction

There are four general-purpose timers embedded in the ESP32. They are all 64-bit generic timers based on 16-bit prescalers and 64-bit auto-reload-capable up/downcounters.

The ESP32 contains two timer modules, each containing two timers. The two timers in a block are indicated by an `x` in TIMGn_1x; the blocks themselves are indicated by an `n`.

**The timers feature:**
- A 16-bit clock prescaler, from 2 to 65536
- A 64-bit time-base counter

Configurable up/down time-base counter: incrementing or decrementing  
Halt and resume of time-base counter  
Auto-reload at alarm  
Software-controlled instant reload  
Level and edge interrupt generation

---

### 10.2 Functional Description

**10.2.1 16-bit Prescaler**

Each timer uses the APB clock (APB_CLK, normally 80 MHz) as the basic clock. This clock is then divided down by a 16-bit prescaler which generates the time-base counter clock (TB_clk). Every cycle of TB_clk causes the time-base counter to increment or decrement by one. The timer must be disabled (TIMGn_Tx_EN is cleared) before changing the prescaler divisor which is configured by TIMGn_Tx_DIVIDER register; changing it on an enabled timer can lead to unpredictable results. The prescaler can divide the APB clock by a factor from 2 to 65536. Specifically, when TIMGn_TxDIVIDER is either 1 or 2, the clock divisor is 2; when TIMGn_TxDIVIDER is 0, the clock divisor is 65536. Any other value will cause the clock to be divided by exactly that value.

**10.2.2 64-bit Time-base Counter**

The 64-bit time-base counter can be configured to count either up or down, depending on whether TIMGn_TxINCREASE is set or cleared, respectively. It supports both auto-reload and software instant reload. An alarm event can be set when the counter reaches a value specified by the software.

---

**Footer:**
Espressif Systems  
223  
[Submit Documentation Feedback](#)  

ESP32 TRM (Version 5.6)