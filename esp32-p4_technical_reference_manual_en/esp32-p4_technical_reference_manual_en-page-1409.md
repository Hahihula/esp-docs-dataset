

# Chapter 23 ## Brown-out Detector

### 23.1 Introduction

The brown-out detector of ESP32-P4 monitors the voltage levels of pins VDD_ANA and VDD_BAT. If the voltage on these pins drops below the predefined threshold (defaulting to 2.4 V), the detector triggers signals to shut down certain power-consuming blocks (e.g., flash), ensuring that the digital module has sufficient time to save and transfer important data.

### 23.2 Feature List

*   Two monitored sources
    *   Monitors the voltage level of pin VDD_ANA, which supplies power to the analog circuit.
    *   Monitors the voltage level of pin VDD_BAT, which connects the external battery to the chip.
*   Two configurable monitoring modes
    *   Mode 0: The brown-out detector triggers interrupts when the brown-out counter reaches the predefined threshold and selects the reset mode according to the configuration.
    *   Mode 1: The brown-out detector triggers a system reset when the voltage falls below the threshold.
*   Configurable voltage-monitoring thresholds and noise tolerance
*   Configurable handling modes for under-voltage events