

# Chapter 9 Interrupt Matrix (INTMTX)

GoBack

From the perspective of the CPU, the interrupt signals from the interrupt matrix become sources and are sent to the CPU core together with the core local interrupt sources.

## 9.2.3 Interrupt Flow in ESP32-H2

Figure 9.2-1 shows the interrupt flow in ESP32-H2.

![Figure 9.2-1. Interrupt Flow in ESP32-H2](image)

### 9.3 Features

The interrupt matrix embedded in ESP32-H2 has the following features:

*   65 peripheral interrupt sources accepted as input
*   28 CPU peripheral interrupts generated to the CPU as output
*   Current interrupt status query of peripheral interrupt sources
*   Multiple interrupt sources mapping to a single CPU interrupt (i.e., shared interrupts)

## 9.4 Architecture

Figure 9.4-1 shows the structure of the interrupt matrix.

You need to configure the **interrupt matrix registers** to map the peripheral interrupt sources to the CPU interrupts. The Interrupt Matrix Controller in Figure 9.4-1 manages the mapping and sends the interrupt status of each interrupt source to the interrupt status registers which belong to the interrupt matrix registers.

![Figure 9.4-1. Interrupt Matrix Structure](image)

Espressif Systems

351
ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback