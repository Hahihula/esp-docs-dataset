**Chapter Title:**
Chapter 26 SDIO Slave Controller (SDIO)

**GoBack Link:** GoBack

---

**Register Section Header and Description for Register 26.34, SLCHOST_CONF_W_REG (0x8C):**

- **SLCHOST_CONF31**: The interrupt vector used by Host to interrupt Slave. This bit will not be cleared automatically.
- **SLCHOST_CONF29**: The interrupt vector used by Host to interrupt Slave. This bit will not be cleared automatically.

**Register Section Header and Description for Register 26.35, SLCHOST_CONF_REG (0x1F0):**

- **SLCHOST_HSPEED_CON_EN**: Set this bit and HINF_HIGHSPEED_ENABLE, then set the EHS (Enable High-Speed) bit in CCCR at the Host side to output the corresponding signal at the rising clock edge.
- **SLCHOST_FRC_POS_SAMP**: Set this bit to sample the corresponding signal at the rising clock edge.
- **SLCHOST_FRC_NEG_SAMP**: Set this bit to sample the corresponding signal at the falling clock edge.
- **SLCHOST_FRC_SDIO20**: Set this bit to output the corresponding signal at the rising clock edge.
- **SLCHOST_FRC_SDIO11**: Set this bit to output the corresponding signal at the falling clock edge.

---

**Section Title:**
26.7 HINF Registers

**Body Text:**

The addresses in this section are relative to the SDIO Slave base address (0x3BFF4_B000) provided in Table 3.3-6 in Chapter 3 System and Memory. The absolute register addresses are listed in Section [26.4 Register Summary](#).

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

**Footer:**
Espressif Systems  
595 ESP32 TRM (Version 5.6)  

**Submit Documentation Feedback Link:** Submit Documentation Feedback