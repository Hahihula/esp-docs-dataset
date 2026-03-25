

```markdown
Chapter 11 Interrupt Matrix

GoBack

Interrupt Matrix Registers
Interrupt Matrix Controller

Peripheral Interrupt Source (0 ~ 83)

CPU Peripheral Interrupt (16 ~ 47)

Figure 11.4-1. Interrupt Matrix Structure

11.5 Functional Description

11.5.1 Peripheral Interrupt Sources

The ESP32-C5 has 84 peripheral interrupt sources in total. Table 11.5-1 lists all these sources and their mapping registers, as well as the interrupt status registers.

*   Column "No.": Peripheral interrupt source number, can be 0 ~ 83.
*   Column "Chapter": in which chapter the interrupt source is described in detail.
*   Column "Interrupt Source": Name of the peripheral interrupt source.
*   Column "Interrupt Source Mapping Register": Registers used to configure the routing of the peripheral interrupt sources to the HP CPU peripheral interrupts.
*   Column "Interrupt Status Register": Registers used to reflect the interrupt source status.

    -   Column "Interrupt Status Register - Bit": Bit position in status registers, indicating the interrupt status.
    -   Column "Interrupt Status Register - Name": Name of status registers.
```