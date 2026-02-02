**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Body Text:**
programmed in the SA register. By setting Bit[30] in the SA register to 1, the MAC Address Register (EMACADDR0 - EMACADDR7) can be configured to contain SA, instead of Destination Address (DA), for filtering. Group filtering with SA is also supported. If the Source Address Filter (SAF) enable bit in the Frame Filter Register is set to 1, the MAC discards frames that do not pass the SAF filtering. Otherwise, the result of SA filtering is given as a status bit in the Receive Status word (Please refer to Table 24.8-5).

When the SAF enable bit is set to 1, the result of the SA filtering and DA filtering is AND’ed to determine whether or not to forward the frame. Any frame that fails to pass will be discarded. Frames need to pass both filterings in order to be forwarded to the application.

**Subheading:**
24.4.5 Inverse Filtering Operation

**Body Text:**
For both destination address (DA) and source address (SA) filtering, you can invert the results matched through the filtering at the final output. The inverse filtering of DA and SA are controlled by the DAIF and SAF bits, respectively, in the Frame Filter Register. The DAIF bit applies to both unicast and multicast DA frames.

When DAIF is set to 1, the result of unicast or multicast destination address filtering will be inverted. Similarly, when the SAIF bit is set to 1, the result of unicast SA filtering is reversed.

The following two tables summarize the destination address and source address filtering, based on the type of frames received:

**Table Title:**
Table 24.4-1. Destination Address Filtering

| Frame Type | PM | PF | DAIF | PAM | DB | DA Filter Result |
|------------|----|----|------|-----|----|------------------|
| Broadcast  |    | X  | X    | X   | X  | Pass             |
|            | O  | X  |      |     |    |                  |
|            | O  | X  |      |     |    | Fail             |
|            | 1  | X  |      |     |    | All frames pass. |
|            | 0  | X  |      |     |    | Pass when results of perfect/group filtering match. |
| Unicast    | O  |   | X    | X   | X  | Fail when results of perfect/group filtering match. |
|            | 1  | C  |      |     |    |                  |
|            | 0  | I  |      |     |    |                  |
| Multicast  | O  |   | O    | O   | X  | Pass when results of perfect/group filtering match and pause control frame is discarded, if PCF = Ox. |
|            | 1  | C  |      |     |    |                  |
|            | 0  | I  |      |     |    |                  |

**Footer Text:**
The filtering parameters in the MAC Frame Filter Register described in Table 24.4-1 are as follows.

**Company Information:**
Espressif Systems

**Document Information:**
ESP32 TRM (Version 5.6)

**Navigation Links:**
GoBack
Submit Documentation Feedback