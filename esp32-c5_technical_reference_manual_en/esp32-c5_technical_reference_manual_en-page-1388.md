

```markdown
If TWAIFD_RTRTH consecutive retransmissions are not successful (error frame or arbitration lost) from a single TX buffer, this TX buffer moves to "TX failed" state. If the TX buffer used for transmission changes between two transmissions (e.g., it is picked due to higher priority), the internal counter of retransmissions is erased and new frames (from new TX buffer) has again TWAIFD_RTRTH + 1 transmission attempts. If CAN FD returns to transmit from original TX buffer, it does not remember the previous number of transmission attempts and again attempts to transmit CAN frames TWAIFD_RTRTH + 1 times. If TX buffer which is currently used for transmission moves to "aborted" state, the internal counter of retransmissions is also erased. If such TX buffer moves to "ready" state again, CAN FD attempts to transmit it TWAIFD_RTRTH + 1 times. The current number of transmission attempts of a single frame is held in an internal counter, which is readable via TWAIFD_RETR_CTR_VAL.

### 38.3.8.5 Abort

If the software driver previously requested transmission of CAN frames by "set ready" command, it can request to abort the transmission by "set abort" command. If the TX buffer is still in "ready" state when it receives "set abort" command (transmission did not start yet), it moves to "aborted" state immediately. If the TX buffer is in "TX in progress" state (transmission has already started), it moves to "abort in progress" state. In such case, it will move to "aborted" state upon the nearest error frame or arbitration lost. Note that when the TX buffer is in "abort in progress" state, it can move to TX OK state if the current transmission succeeds, or to "TX failed state" if retransmission limit is reached.

### 38.3.8.6 TX Buffer Bus-off Behavior

When CAN FD becomes bus-off due to TEC > 255, TX buffers can react to this event in two ways:

1. All TX buffers which are in "ready", "TX in progress" or "abort in progress" immediately go to "TX failed" state. This option is enabled by setting TWAIFD_TBFBO to 1, and it is the default configuration of TX buffers.

2. TX buffer used for transmission at time when CAN FD becomes bus-off will behave as if any other error frame was transmitted. This option is enabled by setting TWAIFD_TBFBO to 0. If no "set abort" command is issued to this buffer, nor retransmission limit is reached, the buffer will become "ready". When CAN FD finishes reintegration (see Section 38.3.4), transmission from this TX buffer will begin as per regular TX buffer selection by priority. This option allows going bus-off and re-integrating without the need of software interaction with TX buffers.

Please refer to Section 38.5.1.1 CAN Frame Transmission for programming procedures.

### 38.3.9 CAN Frame Reception

CAN FD contains a single RX buffer where received CAN frames are stored. RX buffer size is a multiple of 32-bit words, and it can be read from RX_MEM_INFO register. RX buffer is organized like FIFO. The CAN frame is stored to RX buffer when it is received successfully on the CAN bus (no error frames occurred). The CAN frame is read by software from RX buffer by consecutive reads from TWAIFD_RX_DATA. A single read from TWAIFD_RX_DATA reads one word from the RX buffer. The RX buffer operates in one of two modes:

* Automatic mode - When TWAIFD_RX_DATA is read, the read pointer of RX FIFO is automatically incremented. This mode should be used only when TWAIFD_RX_DATA is read by 32-bit access. Writes to TWAIFD_RXRPMV = 1 have no effect in this mode.
```