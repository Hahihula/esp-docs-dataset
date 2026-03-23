

# Chapter 25  
## Clock Glitch Detection  

### 25.1 Overview  

The Clock Glitch Detection module on ESP32-C3 detects glitches in external crystal XTAL_CLK signals, and generates a system reset signal when detecting glitches to reset the whole digital circuit including RTC. By doing so, it prevents attackers from injecting glitches on external crystal XTAL_CLK clock to compromise ESP32-C3 and thus strengthens chip security.  

### 25.2 Functional Description  

#### 25.2.1 Clock Glitch Detection  

The Clock Glitch Detection module on ESP32-C3 monitors input clock signals from XTAL_CLK. If it detects a glitch, namely a clock pulse (a or b in the figure below) with a width shorter than 3 ns, input clock signals from XTAL_CLK are blocked.  

![Figure 25.2-1. XTAL_CLK Pulse Width](image-placeholder)  
XTAL_CLK  

#### 25.2.2 Reset  

Once detecting a glitch on XTAL_CLK that affects the circuit’s normal operation, the Clock Glitch Detection module triggers a system reset if RTC_CNTL_GLITCH_RST_EN bit is enabled. By default, this bit is set to enable a reset.