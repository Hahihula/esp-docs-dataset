

```markdown
Register 52.20. EMACFC_REG (0x0018)

| Bit | 31         | 30-16 | 15   | 14    | 13     | 12      | 11       | 10        | 9          | 8          | 7   | 6   | 5   | 4   | 3   | 2   | 1   | 0   |
|-----|------------|-------|------|-------|--------|---------|----------|-----------|------------|------------|-----|-----|-----|-----|-----|-----|-----|-----|
|     | 0x00000    |       |      |       |        |         |          |           |            |            | O   | OxO | O   | O   | O   | O   | O   | Reset |

PAUSE_TIME Configures the value to be used in the Pause Time field in the transmit control frame.
If the Pause Time bits is configured to be double-synchronized to the (G)MII clock domain, then consecutive writes to this register should be performed only after at least four clock cycles in the destination clock domain. (R/W)

DZPQ Configures whether to disable the automatic generation of the Zero-Quanta Pause Control frames.
0: Enable
1: Disable
(R/W)

PLT Configures the threshold of the PAUSE timer at which the PAUSE Frame is automatically retransmitted.
0: The threshold is Pause time minus 4 slot times (PT - 4 slot times).
1: The threshold is Pause time minus 28 slot times (PT - 28 slot times).
2: The threshold is Pause time minus 144 slot times (PT - 144 slot times).
3: The threshold is Pause time minus 256 slot times (PT - 256 slot times).
The threshold values should be always less than the Pause Time configured in Bits[31:16]. For example, if PT = 100H (256 slot-times), and PLT = 01, then a second PAUSE frame is automatically transmitted 228 (256 - 28) slot times after the first PAUSE frame is transmitted.
(R/W)

UPFD Configures whether to enable unicast pause frame detection.
0: Disable. The MAC only detects Pause frames with a unique multicast address.
1: Enable. The MAC can also detect Pause frames with unicast address of the station. This unicast address should be as specified in the EMACADDRRO High Register and EMACADDRO Low Register.
(R/W)

RFCE Configures whether to enable the decode function of the Pause time.
0: Disable
1: Enable. The MAC decodes the received Pause frame and disables its transmitter for a specified (Pause) time
(R/W)

TFCE Configures whether to enable transmit flow control in full-duplex mode, and whether to enable the back-pressure feature in half-duplex mode.
0: Disable
1: Enable
(R/W)
```