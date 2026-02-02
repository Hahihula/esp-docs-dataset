**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Register Section Header:**
Register 24.9. DMAMISSEDFR_REG (0x0020)

**Table Description and Values for Register Bits:**
- Overflow_BFOC, Overflow_FC, Overflow_BMFC
- Missed_FC

**Field Descriptions with Values in Hexadecimal Format:**
- 30 | 29 | 28 | 27 | 17 | 16 | 10 |
- 0xO | OXO | Reset (indicating the reset value)

**Text Descriptions for Fields and Their Functions:**

- **Overflow_BFOC:** This bit is set every time the Overflow Frame Counter (Bits[27:17]) overflows, that is, the Rx FIFO overflows with the overflow frame counter at maximum value. In such a scenario, the overflow frame counter is reset to all-zeros and this bit indicates that the rollover happened.
  - **(R/SS/RC)**

- **Overflow_FC:** This field indicates the number of frames missed by the application. This counter is incremented each time the MTL FIFO overflows. The counter is cleared when this register is read.
  - **(R/SS/RC)**

- **Overflow_BMFC:** This bit is set every time Missed Frame Counter (Bits[15:0]) overflows, that is, the DMA discards an incoming frame because of the Host Receive Buffer being unavailable with the missed frame counter at maximum value. In such a scenario, the Missed frame counter is reset to all-zeros and this bit indicates that the rollover happened.
  - **(R/SS/RC)**

- **Missed_FC:** This field indicates the number of frames missed by the controller because of the Host Receive Buffer being unavailable. This counter is incremented each time the DMA discards an incoming frame. The counter is cleared when this register is read.
  - **(R/SS/RC)**

**Register Section Header:**
Register 24.10. DMRINTWDTIMER_REG (0x0024)

**Field Description with Values in Hexadecimal Format and Functionality Explanation for RIWC Bit:**

- **RIWC:** This bit indicates the number of system clock cycles multiplied by 256 for which the watchdog timer is set.
  - The watchdog timer gets triggered with the programmed value after the Rx DMA completes the transfer of a frame for which the RI (RECV_INT) status bit is not set because of the setting in the corresponding descriptor RDES[31]. When the watchdog timer runs out, the RI bit is set and the timer is stopped. The watchdog timer is reset when the RI bit is set high because of automatic setting of RI as per RDES[31] of any received frame.
  - **(R/W)**

**Footer Information:**
Espressif Systems
498 ESP32 TRM (Version 5.6)
Submit Documentation Feedback