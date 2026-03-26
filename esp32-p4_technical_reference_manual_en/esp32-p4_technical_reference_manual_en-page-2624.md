

```markdown
| Frame Type | PM | SAIF | SAF | Source Address Filter Operation |
|:-----------|:----|:------|:-----|:----------------------------------|
|            |    |       |      | Pass all frames                   |
| Unicast    | 1  | X     | X    | Pass on perfect/group filter match but do not drop frames that fail |
|            | 0  | O     | O    | Fail on perfect/group filter match but do not drop frames that fail |
|            | 0  | O     |      | Pass on perfect/group filter match and drop frames that fail       |
|            | 0  | O     |      | Fail on perfect/group filter match and drop frames that fail        |

The filtering parameters in the MAC Frame Filter Register described in Table 52.4-15 are as follows.

Parameter name
PM: Pass All Multicast
SAF: Source Address Filtering
SAIF: Source Address Inverse Filtering

Parameter setting
1: Set
0: Cleared
X: Don't care
```

## 52.4.6 Energy Efficient Ethernet (EEE)

Energy Efficient Ethernet (EEE) is an optional operating mode that enables the MAC sublayer along with a series of physical layers to operate in the Low Power Idle (LPI) mode. The EEE mode supports 100 Mbps MAC operations compliant with the IEEE 802.3az-2010 standard. The EEE is supported only in the full-duplex mode when MAC uses MII.

The LPI mode allows power saving by switching off parts of the communication device functionality when there is no data to be transmitted and received. The system on both sides of the link can disable some functionalities and save power during the period of low-link utilization. The MAC controls whether the system should enter or exit the LPI mode and communicate this to the PHY.

### 52.4.6.1 Transmission

To enter the LPI mode, the software must set the `LPIEN` bit to indicate to the MAC to stop transmission and initiate the LPI protocol. The MAC completes the transmission in progress, generates its transmission status, and then starts transmitting the LPI pattern instead of the IDLE pattern during the Interframe gap (IFG). The MAC then updates `TLPIEN` and generates an interrupt.

To exit the LPI mode, the software must clear the `LPIEN` bit to indicate to the MAC. The MAC stops transmitting the LPI pattern, and starts transmitting the IDLE pattern. When the `LPI_TW_TIMER` expires, the MAC updates `TLPIEX` and generates an interrupt.

### 52.4.6.2 Reception

When the PHY receives the signals from the link partner to enter into the LPI state, the PHY starts transmitting the LPI pattern. The MAC updates `RLPIEN` and generates an interrupt.

When the PHY receives signals from the link partner to exit the LPI state, the PHY stops transmitting the LPI pattern. The MAC updates `RLPIEX` and generates an interrupt.

## 52.4.7 Source Address, VLAN, and CRC Control
```