

# Chapter 6

## Reset and Clock

### 6.1 Reset

#### 6.1.1 Overview

ESP32-C3 provides four types of reset that occur at different levels, namely CPU Reset, Core Reset, System Reset, and Chip Reset. All reset types mentioned above (except Chip Reset) maintain the data stored in internal memory. Figure 6.1-1 shows the scope of affected subsystems by each type of reset.

#### 6.1.2 Architectural Overview

![Figure 6.1-1. Reset Types](image-placeholder)

**Legend:**
- CPU Reset
- Core Reset
- System Reset
- Chip Reset

Diagram components:
- **Digital System**: Contains Digital Core (CPU, Peripherals, Digital GPIO)
- **Wi-Fi/Bluetooth LE**: Includes Wi-Fi and Bluetooth LE blocks
- **RTC**: Includes eFuse and PMU modules
- **Analog**

#### 6.1.3 Features

* Support four reset levels:
    - CPU Reset: Only resets CPU core. Once such reset is released, the instructions from the CPU reset vector will be executed.

---

Espressif Systems  
Page 191  
ESP32-C3 TRM (Version 1.3)