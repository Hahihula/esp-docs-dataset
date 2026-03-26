

# Chapter 10

## Reset and Clock

### 10.1 Reset

#### 10.1.1 Overview

ESP32-P4 provides four types of reset that occur at different levels, namely CPU Reset, Core Reset, System Reset, and Chip Reset. All reset types mentioned above (except Chip Reset) preserve the data stored in internal memory. Figure 10.1-1 shows the scopes of affected subsystems by each type of reset.

#### 10.1.2 Architectural Overview

![Figure 10.1-1. Reset Types](#)

ESP32-P4's Digital System consists of High Performance System (HP system) that includes Digital Core and HP memory, and Low Power System (LP system) that includes the Low Power Always On (LP AON) system, LP Core, and LP memory. See Figure 10.1-1 for details (note that HP memory and LP memory would not be reset, so they are not shown in the figure).

#### 10.1.3 Features

* Four reset types:
    * CPU Reset: resets CPU core. HP CPU0, HP CPU1, and LP CPU can be reset independently:

        * HP CPU0 will be automatically released from reset after chip power-up, and start execution from CPU Reset Vector (0x30100000).