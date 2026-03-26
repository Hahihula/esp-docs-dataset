

```markdown
Register 52.21. EMACVLANTAG_REG (0x001C)
```

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 19  | ESVL                                                                        |
| 18  | VTIM                                                                        |
| 17  | ETV                                                                         |
| 16  | VL                                                                          |
| ... |                                                                             |
| 0   | Reset                                                                       |

**ESVL** Configures whether to enable S-VLAN.
- 0: Disable.
- 1: Enable. The MAC transmitter and receiver also consider the S-VLAN (Type = 0x88A8) frames as valid VLAN tagged frames.
(R/W)

**VTIM** Configures whether to enable VLAN Tag inverse match.
- 0: Disable. The frames with matched VLAN Tag are marked as matched.
- 1: Enable. The frames that do not have matching VLAN Tag are marked as matched.
(R/W)

**ETV** Configures whether to enable 12-bit VLAN Tag comparison.
- 0: Disable. All 16 bits of the 15th and 16th bytes of the received VLAN frame are used for comparison and VLAN hash filtering.
- 1: Enable. A 12-bit VLAN identifier is used for comparing and filtering instead of the complete 16-bit VLAN tag. Bits [11:0] of VLAN tag are compared with the corresponding field in the received VLAN-tagged frame.
(R/W)

**VL** Configures the 802.1Q VLAN tag to identify the VLAN frames and is compared to the 15th and 16th bytes of the frames being received for VLAN frames.
When the ETV bit is set, only the VID (Bits[11:0]) is used for comparison.
If VL (VL[11:0] if ETV is set) is all zeros, the MAC does not check the fifteenth and 16th bytes for VLAN tag comparison, and declares all frames with a Type field value of 0x8100 or 0x88a8 as VLAN frames.(R/W)
```