

```markdown
Chapter 10 Interrupt Matrix (INTMTX)
GoBack

Peripheral Interrupt Source
(0~76)

Interrupt Matrix

Interrupt Registers <--> CPU Interrupt Controller

CPU Peripheral Interrupt
(1, 2, 5, 6, 8~31)

Figure 10.2-1. Interrupt Matrix Structure

10.3 Functional Description

10.3.1 Peripheral Interrupt Sources

The ESP32-C6 has 77 peripheral interrupt sources in total. Table 10.3-1 lists all these sources and their mapping/status registers.

*   Column "No.": Peripheral interrupt source number, can be 0 ~ 76.
*   Column "Chapter": in which chapter the interrupt source is described in detail.
*   Column "Interrupt Source": Name of the peripheral interrupt source.
*   Column "Interrupt Source Mapping Register": Registers used for routing the peripheral interrupt sources to CPU peripheral interrupts.
*   Column "Interrupt Status Register": Registers used for indicating the interrupt status of peripheral interrupt sources.

    -   Column "Interrupt Status Register - Bit": Bit position in status register, indicating the interrupt status.
    -   Column "Interrupt Status Register - Name": Name of status registers.
```