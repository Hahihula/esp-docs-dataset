

```markdown
## 38.3.12.4 Bus Monitoring Mode

In bus monitoring mode, CAN FD does not transmit any frames, it only receives CAN frames. If a CAN frame is inserted to TX buffer and "set ready" command is issued, the frame will not be transmitted, and TX buffer will immediately move to "TX failed" state. In bus monitoring mode, CAN FD does not transmit any dominant bit on the bus. If a dominant bit is about to be transmitted on the bus (e.g. ACK or error frame), it is re-routed internally so that CAN FD receives this field, but other nodes on the CAN bus do not see it. Bus monitoring mode is enabled when setting `TWAIFD_BMM` to 1, which can be modified only when CAN FD is disabled (`TWAIFD_ENA = 0`).

## 38.3.12.5 Restricted Operation Mode

In restricted operation mode, CAN FD is able to receive frames on the CAN bus, but it does not transmit any frames. If a CAN frame is inserted to TX buffer and "set ready" command is issued, the frame will not be transmitted, and TX buffer will immediately move to "TX failed" state. In restricted operation mode, CAN FD gives ACK to valid frames, but it does not send error or overload frames. If error or overload condition is detected, CAN FD enters bus integration state, and waits for 11 consecutive recessive bits. REC and TEC counters are not modified, therefore CAN FD will always stay in error active state. Restricted operation mode is enabled when setting `TWAIFD_ROM` to 1, which can be modified only when CAN FD is disabled (`TWAIFD_ENA = 0`).

## 38.3.13 Other Features

### 38.3.13.1 Error Code Capture

CAN FD contains an error code capture register. This register stores the type and bit position of last error on the CAN bus which causes error frame transmission. Error code capture is updated in the sample point of the bit where error is detected. Error code capture is readable via `TWAIFD_ERR_CAPT`. CAN FD standard does not define error types as mutually exclusive (e.g. bit error and stuff error may occur at the same time when the transmitted stuff bit value is corrupted to the opposite value). In such case, the feature captures only one type of error with highest priority. Priorities of error types are defined as (form error having the highest priority):

| Priority | 1             | 2           | 3         | 4       | 5          |
|----------|---------------|-------------|-----------|---------|------------|
| Error Type | Form error    | Bit error   | CRC error | ACK error | Stuff error |

Stuff error which occurs during fixed bit stuffing of CAN FD frames is reported as a form error in the error code capture register.

There is an exception to the above mentioned error priority order. If the dominant stuff bit is sent during the arbitration field and a recessive value is sampled, then this is captured as a stuff error, not a bit error.

### 38.3.13.2 Arbitration Lost Capture

CAN FD contains an arbitration lost capture (ALC) register. This register stores the bit position within CAN arbitration field on which CAN FD lost arbitration last time.
```