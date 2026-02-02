**Chapter Title: Chapter 2 DMA Controller (DMA)**

**GoBack**

**Supported:**
- SPI1_DMA_CHAN_SEL[1:0], SPI2_DMA_CHAN_SEL[1:0] and SPI3_DMA_CHAN_SEL[1:0] in DPORT_SPI_DMA_
- CHAN_SEL_REG must be configured to enable the SPI DMA interface for a specific SPI controller. Each SPI controller corresponds to one domain which has two bits with values 0, 1 and 2. Value 3 is reserved and must not be configured for operation.

**Considering SPI1 as an example:**
- If SPI1_DMA_CHAN_SEL[1:0] = 0, then SPI1 does not use any DMA channel;
- If SPI1_DMA_CHAN_SEL[1:0] = 1, then SPI1 enables DMA channel1;
- If SPI1_DMA_CHAN_SEL[1:0] = 2, then SPI1 enables DMA channel2.

**The SPI_OUTLINK_START bit in SPI_DMA_OUT_LINK_REG and the SPI_INLINK_START bit in SPI_DMA_IN_LINK_REG are used for enabling the DMA Engine. The two bits are self-cleared by hardware. When SPI_OUTLINK_START is set to 1, the DMA Engine starts processing the outbound linked list descriptor and prepares to transmit data. When SPI_INLINK_START is set to 1, then the DMA Engine starts processing the inbound linked-list descriptor and gets prepared to receive data.**

**Software should configure the SPI DMA as follows:**
1. Reset the DMA state machine and FIFO parameters;
2. Configure the DMA-related registers for operation;
3. Configure the SPI-controller-related registers accordingly;
4. Set SPI_USR to enable DMA operation.

---

**Subtitle 2.6 I2S DMA Interface**

The ESP32 integrates two I2S modules, I2S0 and I2S1, each of which is powered by a DMA channel. The REG_I2S_DSCR_EN bit in I2S_FIFO_CONF_REG is used for enabling the DMA operation. ESP32 I2S DMA uses the standard linked-list descriptor to configure DMA operations for data transfer. Burst transfer is supported.

However, unlike the SPI DMA channels, the data size for a single transfer is one word, or four bytes.
- REG_I2S_RX_EOF_NUM[31:0] bit in I2S_RXEOF_NUM_REG is used for configuring the data size of a single transfer operation, in multiples of one word.

I2S_OUTLINK_START bit in I2S_OUT_LINK_REG and I2S_INLINK_START bit in I2S_IN_LINK_REG are used for enabling the DMA Engine and are self-cleared by hardware. When I2S_OUTLINK_START is set to 1, the DMA Engine starts processing the outbound linked-list descriptor and gets prepared to send data. When I2S_INLINK_START is set to 1, the DMA Engine starts processing the inbound linked-list descriptor and gets prepared to receive data.

**Software should configure the I2S DMA as follows:**
1. Configure I2S-controller-related registers;
2. Reset the DMA state machine and FIFO parameters;
3. Configure DMA-related registers for operation;
4. In I2S master mode, set I2S_TX_START bit or I2S_RX_START bit to initiate an I2S operation;

**Footer:**
- Espressif Systems
- Submit Documentation Feedback

**Page Number:** 60  
**Document Version:** ESP32 TRM (Version 5.6)