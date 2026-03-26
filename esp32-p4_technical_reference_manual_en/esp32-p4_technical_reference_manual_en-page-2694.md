

```markdown
## 53.4.1.2 Operation Mode

In Operation mode, the TWAI controller connects to the bus and write-protects all configuration registers to ensure consistency during operation. When in Operation mode, the TWAI controller can transmit and receive messages (including error signaling) depending on which operation sub-mode the TWAI controller was configured with. The TWAI controller supports the following operation sub-modes:

*   **Normal mode:** The TWAI controller can transmit and receive messages including error signals (such as Error and Overload Frames).
*   **Self-test mode:** Self-test mode is similar to Normal mode, but the TWAI controller will consider the transmission of a data or remote frame successful and do not generate an ACK error even if it was not acknowledged. This mode is commonly used during the self-test of a TWAI controller.
*   **Listen-only mode:** The TWAI controller will be able to receive messages, but will remain completely passive on the TWAI bus. Thus, the TWAI controller will not be able to transmit any messages, acknowledgments, or error signals. The error counters will remain frozen. This mode is useful for TWAI bus monitoring.

Note that when exiting Reset mode (i.e., entering Operation mode), the TWAI controller must wait for 11 consecutive recessive bits to occur before fully connecting to the TWAI bus (i.e., being able to transmit or receive).

## 53.4.2 Bit Timing

The operating bit rate of the TWAI controller must be configured whilst the TWAI controller is in Reset mode. The bit rate is configured using `TWAI_BUS_TIMING_O_REG` and `TWAI_BUS_TIMING_1_REG`.

The following Table 53.4-1 illustrates the bit fields of `TWAI_BUS_TIMING_O_REG`. The frequency of the TWAI core clock has multiple clock sources that can be configured by the user as needed. See Chapter 10 Reset and Clock for detailed configuration instructions.

Table 53.4-1. Bit Information of `TWAI_BUS_TIMING_O_REG` (0x18)

| Bit 31-16 | Bit 15   | Bit 14   | Bit 13   | Bit 12   | ...... | Bit 1    | Bit 0 |
|-----------|----------|----------|----------|----------|--------|----------|-------|
| Reserved  | SJW.1    | SJW.O    | BRP.13   | BRP.12   | .......| BRP.1    | BRP.O |

**Notes:**

*   **BRP:** The TWAI Time Quanta clock is derived from the XTAL clock (the default is 40 MHz and is configured). The Baud Rate Prescaler (BRP) field is used to define the prescaler according to the equation below, where `t_Tq` is the Time Quanta clock cycle and `t_CLK` is TWAI core clock cycle:  
    `t_Tq = 2 × t_CLK × (BRP + 1)`
*   **SJW (`tsJW`):** Synchronization Jump Width (SJW) `tsJW` is configured in SJW[1:0] where `tsJW = (SJW[1:0] + 1)`.

The following Table 53.4-2 illustrates the bit fields of `TWAI_BUS_TIMING_1_REG`.
```