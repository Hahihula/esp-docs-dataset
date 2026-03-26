

```markdown
Chapter 12 Interrupt Matrix

GoBack

From the perspective of the interrupt matrix, it receives the interrupt signals sent from peripherals and considers them interrupt sources. The interrupt matrix then outputs CPU peripheral interrupt signals to the CPU.

From the perspective of the CPU, the interrupt signals from the interrupt matrix become interrupt sources and are sent to the CPU core together with the core local interrupt sources.

12.2.3 Interrupt Flow in ESP32-P4

Figure 12.2-1 shows the interrupt flow in ESP32-P4.

![Figure 12.2-1. Interrupt Flow in ESP32-P4](image)

12.3 Features

The interrupt matrix embedded in the ESP32-P4 has the following features:

*   128 peripheral interrupt sources accepted as input
*   32 HP CPU0 peripheral interrupts and 32 HP CPU1 peripheral interrupts generated to HP CPU as output
*   Current interrupt status query for peripheral interrupt sources
*   Multiple interrupt sources mapped to a single HP CPU0 or HP CPU1 interrupt (i.e., shared interrupts)
*   Remapping of HP CPU0 or HP CPU1 User Mode interrupts to Machine Mode interrupts

Figure 12.3-1 shows the structure of the interrupt matrix.
```