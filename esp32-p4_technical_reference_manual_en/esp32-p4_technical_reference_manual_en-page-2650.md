

```markdown
Register 52.16. EMACCONFIG_REG (0x0000)

Continued from the previous page...

EMACBACKOFFLIMIT Configures the back-off limit determining the random integer number (r) of slot time delays (4,096 bit times for 1000 Mbps and 512 bit times for 10/100 Mbps) for which the MAC waits before rescheduling a transmission attempt during retries after a collision.
OO: k = min (n, 10)
O1: k = min (n, 8)
10: k = min (n, 4)
11: k = min (n, 1)

where n = retransmission attempt.

The random integer r takes the value in the range 0 <= r < kth power of 2
Valid only in the half-duplex mode. (R/W)

EMACDEFERRALCHECK Configures whether to enable the deferral check function.
O: Disable
1: Enable
(R/W)

EMACTX Configures whether to enable the transmit state machine of the MAC.
O: Disabled after the completion of the transmission of the current frame, and does not transmit any further frames
1: Enabled for transmission on the MII
(R/W)

EMACRX Configures whether to enable the receiver state machine of the MAC. O: Disabled after the completion of the reception of the current frame, and does not receive any further frames from the MII
1: Enabled for receiving frames from the MII
(R/W)

PLTF Configures the number of preamble bytes that are added to the beginning of every Transmit frame.
O: 7 bytes of preamble
1: 5 byte of preamble
2: 3 bytes of preamble
3: Reserved

The preamble reduction occurs only when the MAC is operating in the full-duplex mode. (R/W)
```