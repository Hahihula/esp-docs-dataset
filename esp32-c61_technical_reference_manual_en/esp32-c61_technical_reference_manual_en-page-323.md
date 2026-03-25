

# Chapter 7

## Reset and Clock

### 7.1 Reset

#### 7.1.1 Overview

ESP32-C61 provides four types of reset that occur at different levels, namely CPU Reset, Core Reset, System Reset, and Chip Reset. All reset types mentioned above (except Chip Reset) preserve the data stored in internal memory. Figure 7.1-1 shows the scopes of affected subsystems by each type of reset.

#### 7.1.2 Architectural Overview

Figure 7.1-1. Reset Types

ESP32-C61's Digital System can be divided into two parts: **High Performance System (HP system)** that includes Digital Core, Wireless Mac and Baseband, and HP SRAM, and **Low Power System (LP system)** that only includes some low-power peripherals and LP SRAM. See Figure 7.1-1 for details (note that HP SRAM and LP SRAM would not be reset, so they are not shown in the figure).

#### 7.1.3 Features

* Four reset types: