

```markdown
- Normal Mode: The TWAI controller can transmit and receive messages including error signals (such as error and overload Frames).
- Self-test Mode: Self-test mode is similar to normal Mode, but the TWAI controller will consider the transmission of a data or remote frame successful and do not generate an ACK error even if it was not acknowledged. This is commonly used when the TWAI controller does self-test.
- Listen-only Mode: The TWAI controller will be able to receive messages, but will remain completely passive on the TWAI bus. Thus, the TWAI controller will not be able to transmit any messages, acknowledgments, or error signals. The error counters will remain frozen. This mode is useful for TWAI bus monitoring.

Note that when exiting Reset Mode (i.e., entering Operation Mode), the TWAI controller must wait for 11 consecutive recessive bits to occur before being able to fully connect the TWAI bus (i.e., be able to transmit or receive).

## 33.4.2 Bit Timing

The operating bit rate of the TWAI controller must be configured whilst the TWAI controller is in Reset Mode. The bit rate is configured using `TWAI_BUS_TIMING_O_REG` and `TWAI_BUS_TIMING_1_REG`, and the two registers contain the following fields:

The following Table 33.4-1 illustrates the bit fields of `TWAI_BUS_TIMING_O_REG`. The frequency of the TWAI core clock has multiple clock sources that can be configured by the user as needed. See Chapter 8 Reset and Clock for detailed configuration instructions.

Table 33.4-1. Bit Information of `TWAI_BUS_TIMING_O_REG` (0x18)

| Bit 31-16 | Bit 15   | Bit 14   | Bit 13    | Bit 12 | ...... | Bit 1     | Bit 0 |
|-----------|----------|----------|-----------|--------|--------|-----------|-------|
| Reserved  | SJW.1    | SJW.O    | BRP.13    | BRP.12 | ...... | BRP.1     | BRP.O |

**Notes:**

- **BRP:** The TWAI Time Quanta clock is derived from the XTAL clock (the default is 40 MHz and is configured). The Baud Rate Prescaler (BRP) field is used to define the prescaler according to the equation below, where `tTq` is the Time Quanta clock cycle and `tCLK` is TWAI core clock cycle:  
  `tTq = 2 × tCLK × (2¹³ × BRP.13 + 2¹² × BRP.12 + 2¹¹ × BRP.11 + ... + 2¹ × BRP.1 + 2⁰ × BRP.O + 1)`

- **SJW:** Synchronization Jump Width (SJW) is configured in SJW.O and SJW.1 where `SJW = (2 × SJW.1 + SJW.O + 1)`.

The following Table 33.4-2 illustrates the bit fields of `TWAI_BUS_TIMING_1_REG`.

Table 33.4-2. Bit Information of `TWAI_BUS_TIMING_1_REG` (0x1c)

| Bit 31-8 | Bit 7   | Bit 6    | Bit 5     | Bit 4   | Bit 3   | Bit 2     | Bit 1     | Bit 0 |
|----------|---------|----------|-----------|---------|---------|-----------|-----------|-------|
| Reserved | SAM     | PBS2.2   | PBS2.1    | PBS2.0  | PBS1.3  | PBS1.2    | PBS1.1    | PBS1.0|

**Notes:**

- **PBS1:** The number of Time Quanta in Phase Buffer Segment 1 is defined according to the following equation: `(8 × PBS1.3 + 4 × PBS1.2 + 2 × PBS1.1 + PBS1.0 + 1)`

- **PBS2:** The number of Time Quanta in Phase Buffer Segment 2 is defined according to the following equation: `(4 × PBS2.2 + 2 × PBS2.1 + PBS2.0 + 1)`
```