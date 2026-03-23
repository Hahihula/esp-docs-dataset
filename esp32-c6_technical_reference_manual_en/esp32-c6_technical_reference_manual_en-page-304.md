

# Chapter 8

## Reset and Clock

### 8.1 Reset

#### 8.1.1 Overview

ESP32-C6 provides four types of reset that occur at different levels, namely CPU Reset, Core Reset, System Reset, and Chip Reset. All reset types mentioned above (except Chip Reset) preserve the data stored in internal memory. Figure 8.1-1 shows the scopes of affected subsystems by each type of reset.

#### 8.1.2 Architectural Overview

![Figure 8.1-1. Reset Types](image)

ESP32-C6's Digital System consists of High Performance System (HP system) that includes Digital Core and Wireless Circuit, and Low Power System (LP system). See Figure 8.1-1 for details.

#### 8.1.3 Features

* Four reset types: