**Title: Chapter 30 SPI Controller (SPI)**

**Subtitle: GoBack**

**Section Title: 30.5.8.1 State Machine**

When GP-SPI works as a master, the state machine controls its various states during data transfer, including configuration (CONF), preparation (PREP), command (CMD), address (ADDR), dummy (DUMMY), data out (DOUT), and data in (DIN) states. GP-SPI is mainly used to access 1/2/4/8-bit SPI devices, such as flash and external RAM; thus the naming of GP-SPI states keeps consistent with the sequence naming of flash and external RAM.

The meaning of each state is described as follows:

**Figure Reference: Figure 30.5-5 shows the workflow of GP-SPI state machine**

1. **IDLE:** GP-SPI is not active or in slave mode.
2. **CONF:** only used in DMA-controlled configurable segmented transfer (valid only for GP-SPI2). Set SPI_USR and SPI_USR_COMMAND to enable this state.

**Note: If the current transfer is a single transfer, it means that the current state of SPI_USR is not enabled; if this state is disabled, it implies no data flow.**

3. **PREP:** prepare an SPI transaction and control SPI CS setup time. Set SPI_USR and SPI_CS_SETUP to enable this state.
4. **CMD:** send command sequence. Set SPI_USR and SPI_USR_COMMAND to enable this state.

5. **ADDR:** send address sequence. Set SPI_USR and SPI_USR_ADDR to enable this state.

6. **DUMMY (wait cycle):** send dummy sequence. Set SPI_USR and SPI_USR_DUMMY to enable this state.
7. **DATA: transfer data.**
   - DOUT: send data sequence. Set SPI_USR and SPI_USR_MOSI to enable this state.
   - DIN: receive data sequence. Set SPI_USR and SPI_USR_MISO to enable this state.

8. **DONE:** control SPI CS hold time. Set SPI_USR to enable this state.

**Footer Information:**
- Page number 1122
- Document version ESP32-S3 TRM (Version 1.7)
- Company name Espressif Systems

**Link Texts: Submit Documentation Feedback**