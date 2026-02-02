**Title: Chapter 26 SDIO Slave Controller (SDIO)**

**Body Text:**
The Slave can also select which edge to drive the output lines, in order to accommodate for any latency caused by the physical signal path. The output timing is shown in Figure **26.3-10**.

![Figure 26.3-10](image) Output Timing Diagram

By default, the GPIO5 strapping value determines the Slave’s output driving edge. However, users can decide the output driving edge by configuring the following registers, with priority from high to low:
1. Set `SLCHOST_FRC_SDIO11` in `SLCHOST_CONF_REG` to output the corresponding signal at the falling clock edge;
2. Set `SLCHOST_FRC_SDIO22` in `SLCHOST_CONF_REG` to output the corresponding signal at the rising clock edge;
3. Set `HINF_HIGHSPEED_ENABLE` in `HINF_CFG_DATA1_REG` and `SLCHOST_SPEED_CON_EN` in `SLCHOST_CONF_REG`, then set the EHS (Enable High-Speed) bit in CCCR at the Host side to output the corresponding signal at the rising clock edge.

`SLCHOST_FRC_SDIO11` and `SLCHOST_FRC_SDIO22` fields are five bits wide. The bits correspond to the CMD line and four DATA lines (0-3). Setting a bit causes the corresponding line to output at the rising clock edge or falling clock edge.

**Subtitle: Notes on priority setting**
The configuration of strapping pins has the lowest priority when controlling the sampling edge or driving edge. The lower-priority configuration takes effect only when the higher-priority configuration is not set. For example, the MTDO strapping value determines the sampling edge only when `SLCHOST_FRC_POS_SAMP` and `SLCHOST_FRC_NEG_SAMP` are not set.

**Subtitle: 26.3.7 Interrupt**
Host and Slave can interrupt each other via the interrupt vector. Both Host and Slave have eight interrupt vectors. The interrupt is enabled by configuring the interrupt vector register (setting the enable bit to 1). The interrupt vector registers can clear themselves automatically, which means one interrupt at a time and no other configuration is required.

**Subtitle: 26.3.7.1 Host Interrupt**
- `SLCOHOST_SLCO_RX_NEW_PACKET_INT` Slave has a packet to send.
- `SLCOHOST_SLCO_TX_OVF_INT` Slave receiving buffer overflow interrupt.
- `SLCOHOST_SLCO_RX_UDF_INT` Slave sending buffer underflow interrupt.
- `SLCOHOST_SLCO_TOHOST_BITn_INT (n: 0 ~ 7)` Slave interrupts Host.

**Subtitle: 26.3.7.2 Slave Interrupt**
- `SLCOINT_SLCO_RX_DSCR_ERR_INT` Slave sending descriptor error.
- `SLCOINT_SLCO_TX_DSCR_ERR_INT` Slave receiving descriptor error.

**Footer:**  
Espressif Systems  
570  
Submit Documentation Feedback  
ESP32 TRM (Version 5.6)