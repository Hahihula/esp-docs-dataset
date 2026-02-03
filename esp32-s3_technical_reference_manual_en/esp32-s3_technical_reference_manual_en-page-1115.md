**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Section Titles and Content:**

### **30.5.4 Transfer Modes**

GP-SPI supports the following transfers when working as a master or a slave.

**Table:** Table 30.5-6. Supported Transfers in Master and Slave Modes

| Mode       | CPU-Controlled Single Transfer | DMA-Controlled Single Transfer | DMA-Controlled Configurable Segmented Transfer | DMA-Controlled Slave Segmented Transfer |
|------------|----------------------------------|-------------------------------|-------------------------------------------------|-----------------------------------------|
| **Master**| Full-Duplex Y                    | Y                             | Y                                               | —                                       |
| Half-Duplex| Y                                | Y                             | Y                                               | —                                       |
| **Slave**  | Full-Duplex Y                    | -                              | Y                                               | Y                                      |
| Half-Duplex| Y                                | Y                             | —                                               | Y                                      |

*Note:* DMA-Controlled Configurable Segmented Transfer is not supported on GP-SPI3.

### **30.5.5 CPU-Controlled Data Transfer**

GP-SPI provides 16 x 32-bit data buffers, i.e., SPI_WO_REG ~ SPI_W15_REG; see Figure 30.5-1. CPU-controlled transfer indicates the transfer, in which the data to send is from GP-SPI data buffer and the received data is stored to GP-SPI data buffer. In such transfer, every single transaction needs to be triggered by the CPU, after its related registers are configured. For such reason, the CPU-controlled transfer is always single transfers (consisting of only one transaction). CPU-controlled transfer supports full-duplex communication.

**Figure:** Figure 30.5-1. Data Buffer Used in CPU-Controlled Transfer

| SPI_WO_REG | ... | SPI_W7_REG | ... | SPI_W8_REG | ... | SPI_W15_REG |
|------------|-----|-----------|-----|-----------|-----|-------------|
| 31         |     |          |    |           |    |            |
| 0          |     |          |    |           |    | High        |

### **30.5.1 CPU-Controlled Master Mode**

In a CPU-controlled master full-duplex or half-duplex transfer, the RX or TX data is saved to or sent from SPI_WO_REG ~ SPI_W15_REG; see Figure 30.5-2 for control which buffers are used.

**Bullet Point:**
- **TX data:** When SPI_USR_MOSI_HIGHPART is cleared (i.e., high part mode is disabled), TX data is from SPI_WO_REG ~ SPI_W15_REG and the data address is incremented by 1 on each byte transferred. If

**Footer Information:**
Espressif Systems  
Page number: 1115  
Document version: ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback