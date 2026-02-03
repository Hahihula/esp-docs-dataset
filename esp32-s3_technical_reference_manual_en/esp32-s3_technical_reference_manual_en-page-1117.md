**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**GoBack Link:** [GoBack](#)

---

**Section Heading:**
30.5.6 DMA-Controlled Data Transfer

**Body Text:**

DMA-controlled transfer refers to the transfer, in which GDMA RX module receives data and GDMA TX module sends data. This transfer is supported both in master mode and in slave mode.

A DMA-controlled transfer can be:
- a single transfer, consisting of only one transaction. GP-SPI supports this transfer both in master and slave modes.
- a configurable segmented transfer, consisting of several transactions (segments). Only GP-SPI2 supports this transfer in master mode. For more information, see Section 30.5.8.5.

A DMA-controlled transfer can be:
- a slave segmented transfer, consisting of several transactions (segments). GP-SPI supports this transfer only in slave mode. For more information, see Section 30.5.9.3

A DMA-controlled transfer needs to be triggered once by CPU. When such transfer is triggered, data is transferred by the GDMA engine from or to the DMA-linked memory, without CPU operation.

DMA-controlled transfer supports full-duplex communication, half-duplex communication and functions described in Section 30.5.8 and Section 30.5.9. Meanwhile, the GDMA RX module is independent from the GDMA TX module, which means there are four kinds of full-duplex communications:
- Data is received in DMA-controlled mode and sent in DMA-controlled code.
- Data is received in DMA-controlled mode but sent in CPU-controlled mode.
- Data is received in CPU-controlled mode but sent in DMA-controlled mode.
- Data is received in CPU-controlled mode and sent in CPU-controlled mode.

---

**Section Heading:**
30.5.6.1 GDMA Configuration

**Body Text:**

Select a GDMA channeln, and configure a GDMA TX/RX descriptor, see Chapter 3 GDMA Controller (GDMA).

Set the bit GDMA_INLINK_START_CHn/GDMA_OUTLINK_START_CHn to start GDMA RX/TX engine.

Before all the GDMA TX buffer is used or the GDMA TX engine is reset, if GDMA_OUTLINK_RESET_CHn is set, a new TX buffer will be added to the end of the last TX buffer in use.
- GDMA RX buffer is linked in the same way as the GDMA TX buffer, by setting GDMA_INLINK_START_CHn or GDMA_INLINK_RESET_CHn.

The TX and RX data lengths are determined by the configured GDMA TX and RX buffer respectively, both of which can be unlimited. 
Initialize GDMA inlink and outlink before GDMA starts. The bits SPI_DMA_RX_ENA and SPI_DMA_TX_ENA in register SPI_DMA_CONFIG_REG should be set, otherwise the read/write data will be stored to/sent from the registers SPI_WO_REG ~ SPI_W15_REG.

In master mode, if GDMA_INSuc_EOF_CHn_INT is set, then the interrupt GDMA_INSuc_EOF_CHn_INT will be triggered when one single transfer or one configurable segmented transfer is finished. 

---

**Footer:**
Espressif Systems  
Page Number 1117 ESP32-S3 TRM (Version 1.7)  

**Action Links:** 
Submit Documentation Feedback