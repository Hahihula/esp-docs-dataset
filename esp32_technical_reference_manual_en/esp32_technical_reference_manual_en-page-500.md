**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.15. EMACCONFIG_REG (0x1000)

**Table Description:**
- The table lists various registers and their bit positions, with corresponding values in hexadecimal format.
- Columns include SAIRC, ASS2KP, EMBACKJABBER, etc.

**Field Descriptions:**

- **SAIRC:** This field controls the source address insertion or replacement for all transmitted frames. Bit[30] specifies which MAC Address register (0 or 1) is used for source address insertion or replacement based on values of Bits [29:28]. It's a read/write bit.
  - `2'b0x`: The input signals mti_sa_ctrl_i and ati_sa_ctrl_i control the SA field generation.

- **Bit[30]:** If Bit[30] is set to O, the MAC inserts the content of the MAC Address register in the SA field for all transmitted frames. When this bit is 1 (MAC), it replaces the content with a specific value.
  - `2'b10`: The input signals mti_sa_ctrl_i and ati_sa_ctrl_i control whether Bit[30] should be set to O or not.

- **Bit[31]:** If Bit[30] is set, this bit determines if the MAC replaces all transmitted frames with a specific value. When it's 0 (MAC), no replacement occurs.
  - `2'b11`: This field controls whether the MAC considers received packets as normal or giant.

- **ASS2KP:** Set when Bit[20] is set, this bit allows for up to 2,000 bytes length of frames. When it's not (JE), all sizes more than 2K are considered.
  - `When Bit[20] = JE`: The MAC considers received packets as giant.

- **EMACWATCHDOG:** This field disables the watchdog timer on the receiver when set to O, allowing up to 16,384 bytes of frames. When reset (Bit is high), it limits frame size.
  - `When this bit is set`: The MAC does not allow more than 2,048 bytes.

- **EMACJABBER:** This field disables the jabber timer on the transmitter when Bit[15] is O; otherwise, frames up to a certain limit (16,383 bytes) can be transferred.
  - `When this bit is set`: The MAC cuts off transmission if more than data size of packets are sent.

- **EMACJUMBOFRAME:** This field allows Jumbo frames when Bit[20] = JE; otherwise, it reports giant frame errors for VLAN tagged frames without exceeding a certain limit (9,018 bytes).
  - `When this bit is set`: The MAC accepts up to 9,018 bytes.

**Footer:**
Continued on the next page...

**Document Footer Information:**
- Page number and version information:
  - "500 ESP32 TRM (Version 5.6)"
  
- Company name at bottom left corner.
- Link for submitting documentation feedback ("Submit Documentation Feedback").