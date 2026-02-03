**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Section Heading and Subheading with Content:**

**31.5.1.2 Operation Mode**

In operation mode, the TWAI controller connects to the bus and write-protect all configuration registers to ensure consistency during operation. When in Operation Mode, the TWAI controller can transmit and receive messages (including error signaling) depending on which operation sub-mode the TWAI controller was configured with. The TWAI controller supports the following operation sub-modes:

- **Normal Mode:** The TWAI controller can transmit and receive messages including error signaling (such as error and overload Frames).
  
- **Self-test Mode:** Self-test mode is similar to normal Mode, but the TWAI controller will consider the transmission of a data or RTR frame successful and do not generate ACK error even if it was not acknowledged. This is commonly used when self-testing the TWAI controller.
  
- **Listen-only Mode:** The TWAI controller will be able to receive messages, but will remain completely passive on the TWAI bus. Thus, the TWAI controller will not be able to transmit any messages, acknowledgments, or error signals. The error counters will remain frozen. This mode is useful for TWAI bus monitoring.

Note that when exiting Reset Mode (i.e., entering Operation Mode), the TWAI controller must wait for 11 consecutive recessive bits to occur before being able to fully connect the TWAI bus (i.e., be able to transmit or receive).

**31.5.2 Bit Timing**

The operating bit rate of the TWAI controller must be configured whilst the TWAI controller is in Reset Mode. The bit rate is configured using `TWAI_BUS_TIMING_0_REG` and `TWAI_BUS_TIMING_1_REG`, and the two registers contain the following fields:

- **Table 31.5-1 illustrates the bit fields of TWAI BUS TIMING O REG:**

| Bit | Bit Information |
|-----|------------------|
| 31-16 | Reserved        |
|      | SJW.1           |
| 14   | SJW.0           |
| ...  | ...             |
| 1    | BRP.2           |
| 0    | BRP.0           |

**Notes:**
- **BRP:** The TWAI Time Quanta clock is derived from the APB clock that is usually 80 MHz. The Baud Rate Prescaler (BRP) field is used to define the prescaler according to the equation below, where \( t_{Tq} \) is the Time Quanta clock cycle and \( t_{CLK} \) is APB clock cycle:
\[ t_{Tq} = 2 \times t_{CLK} \times (2^{12} \times BRP.12 + 2^11 \times BRP.11 + ... + 2^1 \times BRP.1 + 2^0 \times BRP.0 + 1) \]

- **SJW:** Synchronization Jump Width (SJW) is configured in SJW.0 and SJW.1 where SJW = \( (2 \times SJW.1 + SJW.0 + 1) \).

**Table 31.5-2 illustrates the bit fields of TWAI BUS TIMING_1 REG:**

| Bit | Bit Information |
|-----|------------------|
| 31-8 | Reserved        |
|      | SAM             |
| ...  | ...             |
| 0    | PBS1.0          |

**Notes:**  
Espressif Systems  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback]