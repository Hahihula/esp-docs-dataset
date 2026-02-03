**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Section Heading:**
34.6 RAM for Receiving and Sending Data

**Body Text:**
The submodule RAM is a buffer area for sending and receiving data. It can be divided into two units: the one for sending data, and the other is for receiving data. The process of sending and receiving data can also be achieved by the CPU and DMA for reading and writing. The latter method is described in detail in Section 34.8.

**Subsection Heading:**
34.6.1 TX RAM Module

**Body Text:**
There are two ways to enable a write operation: DMA and CPU read/write.
If SDIO-sending is enabled, data can be written to the TX RAM module by APB interface. Data will be written to register `SDHOST_BUFFIFO_REG` from the CPU, directly, by an APB interface.

Another way of data transmission is by DMA.

**Subsection Heading:**
34.6.2 RX RAM Module

**Body Text:**
There are two ways to enable a read operation: DMA and CPU read/write.
When the data path receives data, the data will be written to the RX RAM. Then, these data can be read with the APB method at the reading end. Register `SDHOST_BUFFIFO_REG` can be read by the APB directly.

Another way of receiving data is by DMA.

**Section Heading:**
34.7 DMA Descriptor Chain

**Body Text:**
Each linked list module consists of two parts: the linked list itself and a data buffer. In other words, each module points to a unique data buffer and the linked list that follows the module. Figure 34.7-1 shows the descriptor chain.

**Figure Caption:**
Figure 34.7-1. Descriptor Chain

**Diagram Description (from left to right):**
- `Descriptor 0`
- `Data Buffer0`

- `Descriptor 1`
- `Data Buffer1`

- `Descriptor 2`
- `Data Buffer2`

**Footer Information:**
Espressif Systems
Page number: 1275
Document version and type information at the bottom right corner.