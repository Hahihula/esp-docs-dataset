

# Chapter 19  
## Power Supply Detector  

### 19.1 Overview  

ESP32-C61 has a power supply detector that can monitor the voltage on the power pins related to the on-chip clock and digital circuits. The power supply detector includes a brown-out detector and four voltage glitch detectors. The brown-out detector prevents the SoC from brown-out resets, while the voltage glitch detectors protect the SoC against voltage glitch attacks. The power detector operates in the always-on power domain, allowing it to monitor voltage at any time.  

### 19.2 Features  

- Brown-out detector supports two brown-out detection modes (Mode 0 and Mode 1)  
    - Mode 0 supports:  
        * interrupt generation  
        * RF circuits power-down  
        * flash suspend triggering  
        * system reset  
    - Mode 1 supports:  
        * system reset until the voltage returns to normal  

- Voltage glitch detector can detect voltage glitches lasting 50 ns or longer and trigger a system reset.  

### 19.3 Functional Description  

#### 19.3.1 Architecture  

Figure 19.3-1 shows the architecture of the power supply detector. As shown, the power supply detector consists of one brown-out detector and four voltage glitch detectors.