
```markdown
Since a spurious single-event upset (SEU) in RX buffer RAM can potentially modify FRAME_FORMAT_W[DLC] word of the received frame in RX buffer RAM, it may hamper the length of the RX frame as seen by software driver, and therefore get the RX buffer into inconsistent state where software or driver has read only part of a received frame. In such situation, all further frames read from the RX buffer will be corrupted.

### 38.3.11.2 Parity Protection on TX buffer RAM

When software stores a CAN frame to TX buffer, CAN FD appends a parity bit to each word in the TX buffer RAM. When CAN FD attempts to transmit a frame from TX buffer and detects a parity error in TX buffer RAM, it behaves as follows:

1. If CAN FD detects a parity error in FRAME_FORMAT_W, IDENTIFIER_W, TIMESTAMP_U_W or TIMESTAMP_L_W, it does not attempt to transmit the CAN frame.
2. If CAN FD does not detect parity errors in any of TX buffer words mentioned in previous point, it attempts to transmit the CAN frame.
3. If during transmission of CAN frames CAN FD detects a parity error in any of DATA_1_4_W - DATA_61_64_W words from which it transmits CAN frame data payload, it starts transmitting an error frame.

If CAN FD detects a parity error in TX buffer RAM as described in steps 1 to 3 above, such TX buffer moves to “parity error” state as shown in 38.3-8 and TWAIFD_TXPE bit is set.

If CAN FD detects a parity error in TX buffer, software should write the whole CAN frame to TX buffer again before it attempts to use it for further transmissions.

Writing TWAIFD_CTXPE = 1 by software clears TWAIFD_TXPE bit.

When TWAIFD_PCHKE = 0, CAN FD ignores the parity error detected in TX buffers. TWAIFD_TXPE will not be set, and TWAIFD_CTXPE has no effect and TX buffers do not move to “parity error” state.

CAN FD does not detect parity errors in FRAME_TEST_W. Purpose of FRAME_TEST_W is to intentionally corrupt transmitted frames (e.g. for testing of error scenarios on the CAN bus). Such feature is most likely not useful in applications which require parity protection (high reliability application which aim for fault tolerance).

### 38.3.11.3 TX Buffer Backup Mode

When TWAIFD_TXBBM = 1, CAN FD operates in TX buffer backup mode. In TX buffer backup mode, TX buffers with adjacent indices form pairs as is shown in Figure 38.3-15. For example, if TWAIFD_TXT_BUFFER_COUNT = 8 (CAN FD contains 8 TX buffers) there are 4 TX buffer pairs: 1-2, 3-4, 5-6, 7-8.

| TXT Buffer 2 (backup) | TXT Buffer 4 (backup) | TXT Buffer 6 (backup) | TXT Buffer 8 (backup) |
|----------------------|-----------------------|------------------------|------------------------|
| TXT Buffer 1         | TXT Buffer 3          | TXT Buffer 5           | TXT Buffer 7           |

**Figure 38.3-15. TX buffer pairs**

Operation of CAN FD in TX buffer backup mode provides additional fault tolerance since TX buffer with higher index within TX buffer pairs serves as “backup” in case of parity error in “original” TX buffer. The operation of CAN FD in TX buffer backup mode is shown in Figure 38.3-16.
```