**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Section Heading and Subheading with Content:**

- **Listen Only Mode:** The TWAI controller will be able to receive messages, but will remain completely passive on the TWAI bus. Thus, the TWAI controller will not be able to transmit any messages, acknowledgments, or error signals. The error counters will remain frozen. This mode is useful for TWAI bus monitors.

- **25.5.2 Bit Timing**

  - *Body Text:* 
    The operating bit rate of the TWAI controller must be configured whilst the TWAI controller is in Reset Mode.
    The bit rate configuration is located in TWAI_BUS_TIMING_0_REG and TWAI BUS_TIMING_1_REG, and the two registers contain the following fields:

  - *Table Title:*
    Table 25.5-1 illustrates the bit fields of TWAI BUS_TIMING_0_REG.

  - *Table Content (Bit Fields):*
    | Bit 31-8 | Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
    |----------|-------|-------|-------|-------|-------|-------|-------|-------|
    | Reserved | SJW.1 | SJW.0 | BRP.5 | BRP.4 | BRP.3 | BRP.2 | BRP.1 | BRP.0 |

  - *Notes:*
    - SJW: Synchronization Jump Width (SJW) is configured in SJW.0 and SJW.1 where SJW = (2 x SJW.1 + SJW.0 + 1).
    - BRP: The TWAI Time Quantum clock is derived from a prescaled version of the APB clock that is usually 80 MHz.
      *Equation for t_{Tq}:* 
        \(t_{Tq} = \frac{2}{\text{CLK}} \times (2^5 + BRP.4 + 2^3 + BRP.3 + 2^2 + BRP.2 + 2^1 + BRP.1 + 2^0 + BRP.0 + 1)\)

    - *Table Title:*
      Table 25.5-2 illustrates the bit fields of TWAI BUS_TIMING_1_REG; TWAI Address 0x1c

    - *Table Content (Bit Fields):*
      | Bit 31-8 | Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
      |----------|-------|-------|-------|-------|-------|-------|-------|-------|
      | Reserved | SAM   | PBS2.2| PBS2.1| PBS2.0| PBS1.3| PBS1.2| PBS1.1| PBS1.0 |

  - *Notes:*
    - PBS1: The number of Time Quanta in Phase Buffer Segment 1 is defined according to the following equation:
      \((8 \times \text{PBS1.3} + 4 \times \text{PBS1.2} + 2 \times \text{PBS1.1} + \text{PBS1.0} + 1)\)
    - PBS2: The number of Time Quanta in Phase Buffer Segment 2 is defined according to the following equation:
      \(4 \times \text{PBS2.2} + 2 \times \text{PBS2.1} + \text{PBS2.0} + 1\)
    - SAM: Enables triple sampling if set to 1.
      This is useful for low/medium speed buses where filtering spikes on the bus line is beneficial.

- **25.5.3 Interrupt Management**

  *Body Text:* 
  The ESP32 TWAI controller provides seven interrupts, each represented by a single bit in the TWAI_INT_RAW_REG. For a particular interrupt to be triggered (i.e., its bit in TWAI_INT_RAW_REG set to 1), the interrupt’s corresponding enable bit in TWAI_INT_ENA_REG must be set.

**Footer:**
Espressif Systems
538 ESP32 TRM (Version 5.6)
Submit Documentation Feedback