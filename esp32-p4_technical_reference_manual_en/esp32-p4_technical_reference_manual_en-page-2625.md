

```markdown
Chapter 52 Ethernet Media Access Controller (EMAC)
GoBack

52.4.71 Source Address Control

The software can enable source address insertion or replacement for all or some frames:
* Enable source address insertion or replacement for all frames by configuring SAIRC.
* Enable source address insertion or replacement for the current frame by configuring TDES1[31:29] of the frame. When TDES1[31] is set, MAC_ADDRESS1_HI and EMACADDR1LOW_REG are used for insertion and replacement. When TDES1[31] is cleared, MAC_ADDRESS0_HI and EMACADDROLOW_REG are used for insertion and replacement. When ADDRESS_ENABLE1 is not set, MAC_ADDRESO_HI and EMACADDROLOW_REG are used for insertion and replacement irrespective of TDES1[31].

52.4.7.2 VLAN Control

The software can enable VLAN insertion, replacement, or deletion for all or some frames:
* Enable VLAN insertion, replacement, or deletion for all frames by configuring VLC.
* Enable VLAN insertion, replacement, or deletion for the current frame by configuring TDESO[19:18] of the frame.

52.4.7.3 CRC Control

CRC replacement is a feature that the software can use to indicate the MAC to replace the FCS field of the frame being transmitted with the calculated CRC. This feature can be enabled for the current frame by configuring TDESO[24].

CRC replacement is valid only when MAC does not append CRC (TDES0[27] is set), i.e., when FCS is provided by software in frames transmitted. If source address or VLAN control is enabled, the MAC will replace or append FCS fields with CRC when TDES0[27] is set or cleared respectively.

52.4.8 Time Stamp

The IEEE 1588-2008 standard defines the Precision Time Protocol (PTP) that allows precise clock synchronization in measurement and control systems implemented with technologies such as local computing, network communication and distributed objects. It supports system-wide synchronization accuracy in the sub-microsecond range with a minimum network and local clock computing resources.

52.4.8.1 Transmit Path

The MAC captures a timestamp when the start-of-frame data (SFD) is sent on the MII interface. The frames for which timestamps are captured can be controlled on a per-frame basis. In other words, each transmit frame can be marked to indicate whether a timestamp should be captured for that frame. The MAC does not process the transmitted to identity PTP frames. Rather, it captures the timestamp or not according to the configurations of TDES0[25] by software. The MAC returns the timestamp to the software inside the corresponding transmit descriptor, thus connecting the timestamp automatically to the specific PTP frame. The 64-bit timestamp information is written to the TDES6 and TDES7 fields.

52.4.8.2 Receive Path

The MAC processes the received frames to identify valid PTP frames. The snapshot of the time to be sent to the application can be controlled by software via EMACTSTPCCTRL_REG.
```