**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Section Heading and Subsection with Content:**

#### **27.6 RAM for Receiving and Sending Data**

The submodule RAM is a buffer area for sending and receiving data. It can be divided into two units: the one is for sending data, and the other is for receiving data. The process of sending and receiving data can also be achieved by the CPU and DMA for reading and writing. The latter method is described in detail in Section 27.8.

##### **27.6.1 Transmit RAM Module**

There are two ways to enable a write operation: DMA and CPU read/write.
If SDIO-sending is enabled, data can be written to the transferred RAM module by APB interface or DMA. Data will be written from register EMAC_FIFO to the CPU, directly, by an APB interface.

##### **27.6.2 Receive RAM Module**

There are two ways to enable a read operation: DMA and CPU read/write.
When a subunit of the data path receives data, the subdata will be written onto the receive-RAM. Then, these subdata can be read either with the APB or the DMA method at the reading end. Register EMAC_FIFO can be read by the APB directly.

##### **27.7 Descriptor Chain**

Each linked list module consists of two parts: the linked list itself and a data buffer. In other words, each module points to a unique data buffer and the linked list that follows the module. Figure 27.7-1 shows the descriptor chain.
![Figure 27.7-1. Descriptor Chain](image-reference)

##### **27.8 The Structure of a Linked List**

Each linked list consists of four words. As is shown below, Figure 27.8-1 demonstrates the linked list’s structure, and Table 27.8-1, Table 27.8-2, Table 27.8-3, Table 27.8-4 provide the descriptions of linked lists.

**Footer:**
Espressif Systems
603 ESP32 TRM (Version 5.6)