

```markdown
Chapter 8 Interrupt Matrix (INTERRUPT)

GoBack

## 8.3 Functional Description

### 8.3.1 Peripheral Interrupt Sources

The ESP32-C3 has 62 peripheral interrupt sources in total. Table 8.3-1 lists all these sources and their configuration/status registers.

*   Column "No.": Peripheral interrupt source number, can be 0 ~ 61.
*   Column "Chapter": in which chapter the interrupt source is described in detailed.
*   Column "Source": Name of the peripheral interrupt source.
*   Column "Configuration Register": Registers used for routing the peripheral interrupt sources to CPU peripheral interrupts
*   Column "Status Register": Registers used for indicating the interrupt status of peripheral interrupt sources.

    -   Column "Status Register - Bit": Bit position in status register, indicating the interrupt status.
    -   Column "Status Register - Name": Name of status registers.
```