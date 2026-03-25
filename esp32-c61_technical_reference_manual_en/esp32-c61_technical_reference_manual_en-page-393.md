

# 9.5 Functional Description

## 9.5.1 Peripheral Interrupt Sources

The ESP32-C61 has 66 peripheral interrupt sources in total. Table 9.5-1 lists all these sources and their mapping registers, as well as the interrupt status registers.

*   Column "No.": Peripheral interrupt source number, can be 0 ~ 61.
*   Column "Chapter": in which chapter the interrupt source is described in detail.
*   Column "Interrupt Source": Name of the peripheral interrupt source.
*   Column "Interrupt Source Mapping Register": Registers used to configure the routing of the peripheral interrupt sources to the HP CPU peripheral interrupts.
*   Column "Interrupt Status Register": Registers used to reflect the interrupt source status.

    -   Column "Interrupt Status Register - Bit": Bit position in status registers, indicating the interrupt status.
    -   Column "Interrupt Status Register - Name": Name of status registers.