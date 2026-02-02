**Title:**
Chapter 26 SDIO Slave Controller (SDIO)

**Subtitle:**
26.5 SLC Registers

**Body Text:**
The addresses in this section are relative to the SDIO Slave base address (0x3FF5_8000) provided in Table 3.3-6 in Chapter 3 System and Memory. The absolute register addresses are listed in Section [26.4 Register Summary](#).

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

**Register Information:**
- **Register Name:** SLCCONFO_REG (0x0)

**Table Description:**
The table shows the bit positions and their corresponding register names for various functions related to SDIO Slave Control. The bits are labeled from 31 down to 0, with some being reserved or reset.

**Bit Positions Explanation in Table:**
- **SLCCONFO_SLCO_TOKEN_AUTO_CLR:** Please initialize to O. Do not modify it.
- **SLCCONFO_SLCO_RX_AUTO_WRBACK:** Allows changing the owner bit of the transmitting buffer’s linked list when transmitting data (R/W)
- **SLCCONFO_SLCO_RX_LOOP_TEST:** Loop around when the slave buffer finishes sending packets
  - When set to 1, hardware will not change the owner bit in the linked list.
- **SLCCONFO_SLCO_TX_LOOP_TEST:** Loop around when the slave buffer finishes receiving packets
  - When set to 1, hardware will not change the owner bit in the linked list (R/W)
- **SLCCONFO_SLCO_RX_RST:** Set this bit to reset the transmitting FSM.
- **SLCCONFO_SLCO_TX_RST:** Set this bit to reset the receiving FSM.

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)

**Navigation Links:**
GoBack

**Section Link:**
Submit Documentation Feedback