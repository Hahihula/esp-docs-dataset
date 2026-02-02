**Title: Chapter 26 SDIO Slave Controller (SDIO)**

---

### Figure Caption:
- **Figure 26.3-8. Loading Receiving Buffer**

---

**Body Text:**
The CPU first needs to append new buffer segments at the end of the linked list that is being used by DMA and is available for receiving data.

The CPU then needs to notify the DMA that the linked list has been modified. This can be done by setting bit SLCO_TXLINK_RESTART of the SLCOTX_LINK register. Please note that when the CPU initiates DMA to receive packets for the first time, SLCO_TXLINK_RESTART should be set to 1.

Lastly, the CPU refreshes any available buffer information by writing to the SLCOTOKEN1 register.

---

**Subtitle: SDIO Bus Timing**

**Subsection Title:**
26.3.6 SDIO Bus Timing

**Body Text:**
The SDIO bus operates at a very high speed and the PCB trace length usually affects signal integrity by introducing latency. To ensure that the timing characteristics conform to the desired bus timing, the SDIO Slave module supports configuration of input sampling clock edge and output driving clock edge.

When the incoming data changes near the rising edge of the clock, the Slave will perform sampling on the falling edge of the clock, as Figure 26.3-9 shows.

---

**Figure Caption:**
- **Figure 26.3-9. Sampling Timing Diagram**

---

**Body Text Continued:**
By default, the MTDO strapping value determines the Slave’s sampling edge. However, users can decide the sampling edge by configuring the SLCHOST_CONF_REG register, with priority from high to low:
1. Set SLCHOST_FRC_POS_SAMP to sample the corresponding signal at the rising edge;
2. Set SLCHOST_FRC_NEG_SAMP to sample the corresponding signal at the falling edge.

SLCHOST_FRC_POS_SAMP and SLCHOST_FRC_NEG_SAMP fields are five bits wide. The bits correspond to the CMD line and four DATA lines (0-3). Setting a bit causes the corresponding line to be sampled for input at the rising clock edge or falling clock edge.

---

**Footer:**
Espressif Systems  
569 ESP32 TRM (Version 5.6)  

**Link:** Submit Documentation Feedback