

```markdown
- Software-configurable selection of peripheral requesting its service
- Configurable channel priority and weight arbitration
- Support for memory transfer
- CRC calculation of data
- Interrupt response mechanism for GDMA-AXI linked list switching
```

## 4.3 Architecture

In ESP32-P4, all modules that need high-speed data transfer support GDMA. The GDMA controller and CPU data bus have access to the same address space in memory. Figure 4.3-1 shows the basic architecture of the GDMA controller.

![Figure 4.3-1. GDMA controller Architecture](image_path) *Note: Image not included as per instruction.*

GDMA-AHB and GDMA-AXI have six independent channels respectively, i.e., three transmit channels and three receive channels. Every channel can be connected to different peripherals. In other words, channels are general-purpose, and shared by peripherals.

GDMA-AHB and GDMA-AXI read data from or write data to internal and external memory via AHB_BUS or AXI_BUS respectively. Before this, GDMA uses configurable arbitration schemes for channels requesting read or write access. For the available address range of internal and external memory, please see Chapter 7 System and Memory.

Software can use the GDMA through linked lists. GDMA-AHB linked lists are stored in internal memory, while GDMA-AXI linked lists are stored in internal or external memory. These linked lists consist of outlinkn and inlinkn, where n indicates the channel number (ranging from 0 to 2). The GDMA reads an outlinkn (i.e., a linked list of transmit descriptors) from memory and transmit data in corresponding memory according to the outlinkn, or read an inlinkn (i.e., a linked list of receive descriptors) and store received data into specific address space in memory according to the inlinkn.
```