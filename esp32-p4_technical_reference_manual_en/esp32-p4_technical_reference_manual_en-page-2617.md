

```markdown
| Bits | Name                  | Description                                                                                                                                                                                                 |
|------|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [2:0] | IP Payload Type       | These bits indicate the type of payload encapsulated in the IP datagram processed by the Receive Checksum Offload Engine (COE). The COE also sets these bits to 00 if it does not process the IP datagram's payload due to an IP header error or fragmented IP.<ul><li>000: Unknown or did not process IP payload</li><li>001: UDP</li><li>010: TCP</li><li>011: ICMP</li><li>1xx: Reserved</li></ul>This bit is valid when either Bit[7] or Bit[6] is set. |

Table 52.4-12. Receive Descriptor 6 (RDES6)

| Bits | Name                                  | Description                                                                                                                                                                                                 |
|------|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [31:0]| RTSH: Receive Frame Time Stamp Low    | This field is updated by DMA with the least significant 32 bits of the timestamp captured for the corresponding receive frame. This field is updated by DMA only for the last descriptor of the receive frame which is indicated by the Last Descriptor status bit (RDES0[8]). |

Table 52.4-13. Receive Descriptor 7 (RDES7)

| Bits | Name                                  | Description                                                                                                                                                                                                 |
|------|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [31:0]| RTSH: Receive Frame Timestamp High   | This field is updated by DMA with the most significant 32 bits of the timestamp captured for the corresponding receive frame. This field is updated by DMA only for the last descriptor of the receive frame which is indicated by the Last Descriptor status bit (RDES0[8]). |

## 52.4.4 PHY Interface

The MAC and the external PHY communicate through two interfaces:

* Media Independent Interface (MII)
* Reduced Media Independent Interface (RMII)

### 52.4.4.1 Media Independent Interface: MII

The Media Independent Interface (MII) defines the interconnection between MAC sublayers and PHYs at 10 Mbit/s and 100 Mbit/s.

## MII Signals to PHY

The MII interface signals are shown in Figure 52.4-3.
```