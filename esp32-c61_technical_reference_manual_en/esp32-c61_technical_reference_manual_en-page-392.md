

Chapter 9 Interrupt Matrix

GoBack

From the perspective of the CPU, the interrupt signals from the interrupt matrix become sources and are sent to the CPU core together with the core local interrupt sources.

9.2.3 Interrupt Flow in ESP32-C61

Figure 9.2-1 shows the interrupt flow in ESP32-C61.

```markdown
Peripherals
Peripheral's internal interrupt (sources) → 66 interrupt (signals)
→ 66 peripheral interrupt (sources)

Interrupt Matrix
→ Interrupt Matrix Controller
→ 32 CPU peripheral interrupt (signals)
→ 32 CPU peripheral interrupt (sources)

CPU
2 core local interrupt (sources) (CLINT)
→ CPU Interrupt Controller
```

Figure 9.2-1. Interrupt Flow in ESP32-C61

9.3 Features

The interrupt matrix embedded in the ESP32-C61 has the following features:

*   66 peripheral interrupt sources accepted as input
*   32 HP CPU peripheral interrupts generated to the HP CPU as output
*   Current interrupt status query of peripheral interrupt sources
*   Multiple interrupt sources mapping to a single HP CPU interrupt (i.e., shared interrupts)

9.4 Architecture

Figure 9.4-1 shows the structure of the interrupt matrix.

You need to configure the interrupt matrix registers to map the peripheral interrupt sources to the HP CPU interrupts. The Interrupt Matrix Controller in Figure 9.4-1 manages the mapping and sends the interrupt status of each interrupt source to the interrupt status registers which belong to the interrupt matrix registers.

```markdown
Interrupt Matrix
├── Interrupt Matrix Registers
└── Interrupt Matrix Controller

Peripheral Interrupt Source (0 ~ 65) → Interrupt Matrix Controller → CPU Peripheral Interrupt (16 ~ 47)
```

Figure 9.4-1. Interrupt Matrix Structure