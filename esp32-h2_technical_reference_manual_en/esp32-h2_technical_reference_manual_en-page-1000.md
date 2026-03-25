

```markdown
- BRP: The TWAI Time Quanta clock is derived from the XTAL clock (the default is 40 MHz and is configured). The Baud Rate Prescaler (BRP) field is used to define the prescaler according to the equation below, where tTq is the Time Quanta clock cycle and tCLK is TWAI core clock cycle:  
  `tTq = 2 × tCLK × (2^13 × BRP.13 + 2^12 × BRP.12 + 2^11 × BRP.11 + ... + 2^1 × BRP.1 + 2^0 × BRP.0 + 1)`  
- SJW: Synchronization Jump Width (SJW) is configured in SJW.0 and SJW.1 where `SJW = (2 × SJW.1 + SJW.0 + 1)`.

The following Table 34.4-2 illustrates the bit fields of TWAI_BUS_TIMING_1_REG.

Table 34.4-2. Bit Information of TWAI_BUS_TIMING_1_REG (0x1c)

| Bit 31-8 | Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|----------|-------|-------|-------|-------|-------|-------|-------|-------|
| Reserved | SAM   | PBS2.2| PBS2.1| PBS2.0| PBS1.3| PBS1.2| PBS1.1| PBS1.0|

Notes:

- PBS1: The number of Time Quanta in Phase Buffer Segment 1 is defined according to the following equation: `(8 × PBS1.3 + 4 × PBS1.2 + 2 × PBS1.1 + PBS1.0 + 1)`.
- PBS2: The number of Time Quanta in Phase Buffer Segment 2 is defined according to the following equation: `(4 × PBS2.2 + 2 × PBS2.1 + PBS2.0 + 1)`.
- SAM: Enables triple sampling if set to 1. This is useful for low/medium speed buses to filter spikes on the bus line.

34.4.3 Interrupt Management

The ESP32-H2 TWAI controller provides eight interrupts, each represented by a single bit in TWAI_INT_ST_REG. For a particular interrupt to be triggered, the corresponding enable bit in TWAI_INT_ENA_REG must be set.

The TWAI controller provides the following interrupts:

- Receive Interrupt
- Transmit Interrupt
- Error Warning Interrupt
- Data Overrun Interrupt
- Error Passive Interrupt
- Arbitration Lost Interrupt
- Bus Error Interrupt
- Bus Idle Status Interrupt

The TWAI controller’s interrupt signal to the interrupt matrix will be asserted whenever one or more interrupt bits are set in the TWAI_INT_ST_REG, and deasserted when all bits in TWAI_INT_ST_REG are cleared. The majority of interrupt bits in TWAI_INT_ST_REG are automatically cleared when the register is read, except for the Receive Interrupt which can only be cleared when all the messages are released by setting the TWAI_RELEASE_BUF bit.
```