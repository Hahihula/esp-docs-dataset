

```markdown
Chapter 52 Ethernet Media Access Controller (EMAC) GoBack

Register 52.17. EMACFF_REG (0x0004)

| Bit | Description |
|-----|-------------|
| 31-30 | RECEIVE_ALL (reserved) |
| 17-16 | VTFE (reserved) |
| 15   | PCF |
| 10-9  | SAFE |
| 8    | SAIF |
| 7    | DBF |
| 6    | PAM |
| 5    | DAIF |
| 4-2  | (reserved) |
| 1    | PMODE |
| 0    | Reset |

RECEIVE_ALL Configures whether to pass all received modules.
O: The MAC Receiver module passes only those frames to the Application that pass the SA or DA address filter.
1: The MAC Receiver module passes all received frames, irrespective of whether they pass the address filter or not, to the Application. The result of the SA or DA filtering is updated (pass or fail) in the corresponding bits in the Receive Status Word.
(R/W)

VTFE Configures whether to enable the VLAN Tag filter.
O: Disable. In this case, the MAC forwards all frames irrespective of the match status of the VLAN Tag.
1: Enable. In this case, the MAC drops VLAN-tagged frames that do not match the VLAN Tag comparison.
(R/W)

SAFE Configures whether to enable the source address filter.
O: Disable. In this case, the MAC forwards the received frame to the application with an updated SAF bit of the RX Status depending on the SA address comparison.
1: Enable. In this case, the MAC compares the SA field of the received frames with the values programmed in the enabled SA registers. If the comparison fails, the MAC drops the frame.
(R/W)

SAIF Configures whether to enable SA inverse filtering.
O: Disable. In this case, frames whose SA does not match the SA registers are marked as failing the SA Address filter.
1: Enable. In this case, the Address Check block operates in inverse filtering mode for the SA address comparison. The frames whose SA matches the SA registers are marked as failing the SA Address filter.
(R/W)

Continued on the next page...
```