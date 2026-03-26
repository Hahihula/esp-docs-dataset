

```markdown
Register 52.17. EMACFF_REG (0x0004)
```

## Continued from the previous page...

### PCF
Configures the forwarding of all control frames (including unicast and multicast PAUSE frames).
- O: The MAC filters all control frames.
- 1: The MAC forwards all control frames except PAUSE control frames to application even if they fail the Address filter.
- 2: The MAC forwards all control frames to application even if they fail the Address Filter.
- 3: The MAC forwards control frames that pass the Address Filter.

The following conditions should be true for the PAUSE control frames processing:
- Condition 1: The MAC is in the full-duplex mode and flow control is enabled by setting Bit 2 (RFE) of Register 6 (Flow Control Register) to 1.
- Condition 2: The destination address (DA) of the received frame matches the special multicast address or EMACADDR0 when Bit 3 (UP) of the Register 6 (Flow Control Register) is set.
- Condition 3: The Type field of the received frame is 0x8808 and the OPCODE field is 0x0001.

(R/W)

### DBF
Configures whether to disable broadcast frames.
- O: Enable. The AFM (Address Filtering Module) module passes all received broadcast frames.
- 1: Disable. The AFM module filters all incoming broadcast frames. In addition, it overrides all other filter settings.

(R/W)

### PAM
Configures whether to pass all multicast frames.
- O: Filtering of multicast frame depends on HMC bit
- 1: All received frames with a multicast destination address (first bit in the destination address field is '1') are passed

(R/W)

### DAIF
Configures whether to enable DA inverse filtering for both unicast and multicast frames.
- O: Disable
- 1: Enable

(R/W)

### PMODE
Configures whether to enable the promiscuous mode.
- O: Disable.
- 1: Enabled. In this case, the Address Filter module passes all incoming frames regardless of its destination or source address. The SA or DA Filter Fails status bits of the Receive Status Word are always cleared when PR (PRI_RATIO) is set.

(R/W)
```