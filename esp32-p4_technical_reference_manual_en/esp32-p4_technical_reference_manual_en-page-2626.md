

```markdown
Chapter 52 Ethernet Media Access Controller (EMAC)

The MAC returns the timestamp to the software inside the corresponding receive descriptor. The extended status (including the timestamp status and IPC status) is written to RDES4, and the timestamp snapshot is written to RDES6 and RDES7.

## 52.4.9 Remote Wakeup

The MAC supports remote wakeup. When the receiver receives a remote wakeup frame or a magic packet, an interrupt will be triggered, and the PMU will be notified to wake up the SoC system.

The software can control whether to use remote wakeup frames to trigger interrupts by configuring RWKPKTEN , whether to use magic packets to trigger interrupts by configuring MGKPKTEN, and whether the MAC drops all received frames in power-down mode by configuring PWRDWN.

## 52.4.10 Good Transmitted and Received Frames

A frame that has been successfully transmitted is considered a “good frame”. In other words, a transmitted frame is considered to be “good”, if the frame transmission is not aborted due to the following errors:

*   Jabber timeout (TDES0[14])
*   No carrier or loss of carrier (TDES0[11:10])
*   Late collision (TDES0[9])
*   Frame underflow (TDES0[1])
*   Excessive deferral (TDES0[2])
*   Excessive collision (TDES0[8])

A received frame is considered to be “good” if the following errors do not occur:

*   CRC error (RDES0[1])
*   Runt frames (frames shorter than 64 bytes)
*   Alignment error (in 10/100 Mbps modes only) (RDES0[2])
*   Length error (non-type frames only) (RDES0[12])
*   Frame size over the maximum size (for non-type frames over the maximum frame size only)) (RDES0[7])
*   MII_RXER input error (RDES0[3])

The maximum frame size depends on the frame type:

*   The maximum size of untagged frames = 1518 bytes
*   The maximum size of VLAN frames = 1522 bytes

## 52.5 Programming Procedures

### 52.5.1 MAC System Layer Configuration

1.  Configure the IO interfaces. For detailed configurations about the MII and the RMII interface, see Chapter 9 GPIO Matrix and IO MUX.
```