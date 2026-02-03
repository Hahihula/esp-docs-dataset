**Title:**
4 Functional Description

**Table Headers:**  
Interface | Signal | Pin | Function

**Table Content (Partial):**

- **SPI Interface**:  
  - SPIHD, SD_DATA_2
  - SPIWP, SD_DATA_3
  - SPICSO, SD_CMD
  - SPICLK, SD_CLK
  - SPIQ, SD_DATA_0
  
- **Parallel QSPI**:  
  - HSPICLK, MTMS
  - HSPICSD, MTDQ
  - HSPIQ, MTDI

**Additional Information:**
- Supports Standard SPI, Dual SPI, and Quad SPI that can be connected to the external flash and SRAM.

- **EMAC Interface**:  
  - EMAC_TX_CLK, GPIO05
  - EMAC_RX_CLK, GPIO5
  - EMAC_TX_EN, GPIO21
  - EMAC_TXD0, GPIO19

**Additional Information:**
- Ethernet MAC with MII/RMII interface.

**Footer:**  
Espressif Systems  
Submit Documentation Feedback  
ESP32 Series Datasheet v5.2