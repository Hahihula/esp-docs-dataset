

```markdown
Register 52.49. EMACTXVLTCTRL_REG (0x0584)

CSVL Configures which type is inserted or replaced in the 13th and 14th bytes of transmitted frames.
O: C-VLAN type (0x8100)
1: S-VLAN type (0x88A8)
(R/W)

VLP Configures what controls VLAN deletion, insertion, or replacement.
O: The control input signal
1: VLC
(R/W)

VLC Configures the VLAN tag in transmit frames.
O: No VLAN tag deletion, insertion, or replacement.
1: VLAN tag deletion. The MAC removes the VLAN type (bytes 13 and 14) and VLAN tag (bytes 15 and 16) of all transmitted frames with VLAN tags.
2: VLAN tag insertion. The MAC inserts VLT in bytes 15 and 16 of the frame after inserting the Type value (0x8100/0x88a8) in bytes 13 and 14. This operation is performed on all transmitted frames, irrespective of whether they already have a VLAN tag.
3: VLAN tag replacement. The MAC replaces VLT in bytes 15 and 16 of all VLAN-type transmitted frames (Bytes 13 and 14 are 0x8100/0x88a8).
(R/W)

VLT Configures the value of the VLAN tag to be inserted or replaced.
The value must only be changed when the transmit lines are inactive or during the initialization phase. (R/W)
```