

# Chapter 11 Interrupt Matrix

GoBack

From the perspective of the CPU, the interrupt signals from the interrupt matrix become sources and are sent to the CPU core together with the core local interrupt sources.

## 11.2.3 Interrupt Flow in ESP32-C5

Figure 11.2-1 shows the interrupt flow in ESP32-C5.

![Figure 11.2-1. Interrupt Flow in ESP32-C5](image)

### 11.3 Features

The interrupt matrix embedded in the ESP32-C5 has the following features:

*   84 peripheral interrupt sources accepted as input
*   32 HP CPU peripheral interrupts generated to the HP CPU as output
*   Current interrupt status query of peripheral interrupt sources
*   Multiple interrupt sources mapping to a single HP CPU interrupt (i.e., shared interrupts)
*   Delegation of CPU User Mode interrupts to Machine Mode interrupts

## 11.4 Architecture

Figure 11.4-1 shows the structure of the interrupt matrix.

You need to configure the **interrupt matrix registers** to map the peripheral interrupt sources to the HP CPU interrupts. The Interrupt Matrix Controller in Figure 11.4-1 manages the mapping and sends the interrupt status of each interrupt source to the interrupt status registers which belong to the interrupt matrix registers.