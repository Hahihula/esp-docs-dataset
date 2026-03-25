

```markdown
Figure 38.3-2. Operating modes


When CAN FD is error-active, it takes part in CAN bus communication. If CAN FD becomes error-passive and later bus-off, it stops communicating on the CAN bus and waits before starting reintegration until it receives the error counter reset command (writing 1 to TWAIFD_ECRST). Upon this command, CAN FD starts reintegration. Reintegration lasts until CAN FD detects 129 sequences of 11 consecutive recessive bits (an implementation choice, exceeding the CAN specification minimum of 128 sequences). After 129 such sequences, CAN FD becomes error-active again.

CAN FD can be disabled at any time by writing logic 0 to TWAIFD_ENA register. In such case:

*   CAN FD immediately stops communication on the CAN bus, and transmits only recessive bits.
*   TX/RX error counters (TEC/REC) are reset to 0, CAN FD becomes bus-off.
*   All TX buffers move to “empty” state (see Figure 38.3-8), content of TX buffer RAM remains valid (memories are not reset).
*   The RX buffer is flushed (see Section 38.3.9.5 Flush).

It is recommended for CAN FD not to transmit any frame when it is disabled by clearing TWAIFD_ENA, as this would result in transmission of error frames by other nodes on the CAN bus. Therefore, software driver operating on CAN FD should ensure that none of TX buffers within CAN FD is in “ready”, “TX in progress” or “abort in progress” states (see Section 38.3.8 CAN Frame Transmission).

TWAIFD_ECRST is “sticky”. This means that if CAN FD is not yet bus-off, and this command is issued, CAN FD will remember the command and automatically start reintegration upon nearest transition to bus-off. This way, the command can be issued in advance during communication, and CAN FD will re-integrate as quickly as possible after becoming bus-off, without software additional delay caused by interaction with software driver.

38.3.5 Initialization Sequence

Initialization sequence consists of the following steps:

1.  Reset (either HW reset or soft reset)
```