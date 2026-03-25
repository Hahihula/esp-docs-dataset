

```markdown
Chapter 38 Controller Area Network Flexible Data-Rate (CAN FD) GoBack

PCR_TWAI_FUNC_CLK_SEL
                      |
XTAL_CLK --------------> Clock Mux ---------------- PCR_TWAI_FUNC_CLK_EN --> TWAI_CLK
PLL_80M               |                                |
                     Figure 38.3-1. TWAI_CLK Diagram

38.3.2 Reset

After power-up, CAN FD should be reset either by hardware (HW reset) or by software (soft reset). The soft reset is executed by writing 1 to TWAIFD_RST. If an HW reset is issued to CAN FD, it cannot be accessed for two system clock periods. For example, if CAN FD system clock is 100 MHz, software should wait 20 ns after HW reset is released. If soft reset is issued, no waiting is required. Both HW reset and soft reset have the same effect. By applying any reset, CAN FD is put in the following state:

*   CAN FD is disabled, it does not communicate on the CAN bus (bus-off state).
*   All memory registers within CAN FD are at the reset value.
*   Memories in CAN FD (TX buffer and RX buffer) are not reset.

38.3.3 Time Base

CAN FD integrates an independent 32-bit timer that can generate timestamps, to provide a time base for time triggered transmission or reception of frames. The time base timer can be enabled by configuring TWAIFD_TIMER_CE, and its current value can then be read from TWAIFD_TIMESTAMP_HIGH and TWAIFD_TIMESTAMP_LOW.

The time base is an unsigned timer that counts upward. TWAIFD_TIMER_STEP configures the timing step, TWAIFD_TIMER_LD_VAL_L configures the timer pre-load value, and TWAIFD_TIMER_CT_VAL_L configures the timer count-to value. The valid bit width of the timer can be read from or configured via TWAIFD_TS_BITS, with a range from 1 to 32.

38.3.4 Operating Modes

After reset, CAN FD is disabled, it does not take part in communication on the CAN bus (no transmission, reception, monitoring). Before CAN FD is enabled, it must be configured as explained in Section 38.3.7 CAN Bus Configuration. Once configured, it can be enabled by writing 1 to TWAIFD_ENA. When TWAIFD_ENA = 1, CAN FD starts bus integration and joins the CAN bus communication after receiving 11 consecutive recessive bits. When CAN FD joins CAN bus communication, it becomes error-active (during integration it is bus-off). At this moment CAN FD starts communicating on the CAN bus. The moment when CAN FD joins CAN bus communication can be determined by FCS interrupt and subsequent probing of TWAIFD_EWL_ERP_FAULT_STATE_REG (see Section 38.4 Interrupts). Basic operating modes of CAN FD are shown in Figure 38.3-2.
```