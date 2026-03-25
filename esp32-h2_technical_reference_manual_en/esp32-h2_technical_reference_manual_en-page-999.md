
```markdown
## 34.4.1 Modes

The ESP32-H2 TWAI controller has two working modes: Reset mode and Operation mode. Reset mode and Operation mode are entered by setting or clearing the `TWAI_RESET_MODE` bit.

### 34.4.1.1 Reset Mode

Entering Reset mode is required in order to modify the various configuration registers of the TWAI controller. When entering Reset mode, the TWAI controller is essentially disconnected from the TWAI bus. When in Reset mode, the TWAI controller will not be able to transmit any messages (including error signals). Any transmission in progress is immediately terminated. Likewise, the TWAI controller will not be able to receive any messages either.

### 34.4.1.2 Operation Mode

In Operation mode, the TWAI controller connects to the bus and write-protects all configuration registers to ensure consistency during operation. When in Operation mode, the TWAI controller can transmit and receive messages (including error signaling) depending on which operation sub-mode the TWAI controller was configured with. The TWAI controller supports the following operation sub-modes:

*   **Normal mode:** The TWAI controller can transmit and receive messages including error signals (such as Error and Overload Frames).
*   **Self-Test mode:** Self-test mode is similar to Normal mode, but the TWAI controller will consider the transmission of a data or remote frame successful and not generate an ACK error even if it was not acknowledged. This mode is commonly used during the self-test of a TWAI controller.
*   **Listen-Only mode:** The TWAI controller will be able to receive messages, but will remain completely passive on the TWAI bus. Thus, the TWAI controller will not be able to transmit any messages, acknowledgments, or error signals. The error counters will remain frozen. This mode is useful for TWAI bus monitoring.

Note that when exiting Reset mode (i.e., entering Operation mode), the TWAI controller must wait for 11 consecutive recessive bits to occur before fully connecting to the TWAI bus (i.e., being able to transmit or receive).

## 34.4.2 Bit Timing

The operating bit rate of the TWAI controller must be configured whilst the TWAI controller is in Reset mode. The bit rate is configured using `TWAI_BUS_TIMING_O_REG` and `TWAI_BUS_TIMING_1_REG`, and the two registers contain the following fields:

The following Table 34.4-1 illustrates the bit fields of `TWAI_BUS_TIMING_O_REG`. The frequency of the TWAI core clock has multiple clock sources that can be configured by the user as needed. See Chapter 7 Reset and Clock for detailed configuration instructions.

Table 34.4-1. Bit Information of `TWAI_BUS_TIMING_O_REG` (0x18)

| Bit 31-16 | Bit 15   | Bit 14 | Bit 13 | Bit 12 | ...... | Bit 1 | Bit 0 |
|-----------|----------|--------|--------|--------|--------|-------|-------|
| Reserved  | SJW.1    | SJW.O  | BRP.13 | BRP.12 | ....... | BRP.1 | BRP.0 |

**Notes:**
```