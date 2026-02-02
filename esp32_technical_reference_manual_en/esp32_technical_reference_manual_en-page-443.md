**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Register Information for Register 22.24, I2S_LC_CONF_REG (0x0060):**

- **Field Descriptions and Values in Binary:**
  - `I2S_CHECK_OWNER`: Set this bit to check the owner bit by hardware.
    - Value Range: [0, 1]
  - `I2S_OUT_DATA_BURST_EN`: Transmitter data transfer mode configuration bit. (R/W)
    - Values:
      - "1": Transmit data in burst mode;
      - "0": Transmit data in byte mode.
  - `I2S_INDESCR_BURST_EN`: DMA inlink descriptor transfer mode configuration bit. (R/W)
    - Values:
      - "1": Transfer inlink descriptor in burst mode;
      - "0": Transfer inlink descriptor in byte mode.
  - `I2S_OUTDSCR_BURST_EN`: DMA outlink descriptor transfer mode configuration bit. (R/W)
    - Values:
      - "1": Transfer outlink descriptor in burst mode;
      - "0": Transfer outlink descriptor in byte mode.
  - `I2S_OUT_EOF_MODE`: DMA I2S_OUT_EOF_INT generation mode. (R/W)
    - Values:
      - "1": When DMA has popped all data from the FIFO;
      - "0": When AHB has pushed all data to the FIFO.
  - `I2S_OUT_AUTO_WRBACK`: Set this bit to enable automatic outlink-writeback when all the data in tx buffer has been transmitted. (R/W)
  - `I2S_OUT_LOOP_TEST`: Set this bit to loop test outlink. (R/W)
  - `I2S_IN_LOOP_TEST`: Set this bit to loop test inlink. (R/W)
  - `I2S_AHBM_RST`: Set this bit to reset AHBI interface of DMA. (R/W)
  - `I2S_AHBM_FIFO_RST`: Set this bit to reset AHB interface cmdFIFO of DMA. (R/W)
  - `I2S_OUT_RST`: Set this bit to reset out DMA FSM. (R/W)
  - `I2S_IN_RST`: Set this bit to reset in DMA FSM. (R/W)

**Register Information for Register 22.25, I2S_LC_STATEO_REG (0x006c):**

- **Field Description:**
  - `I2S_LC_STATEO_REG`: Receiver DMA channel status register.
    - Access Mode: Read Only

**Footer Information:**
- Page Number: 443
- Document Title: ESP32 TRM (Version 5.6)
- Company Name: Espressif Systems
- Link Texts:
  - "Submit Documentation Feedback"