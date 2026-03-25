

```markdown
- Three transmit channels and three receive channels
- Software-configurable selection of peripheral requesting its service
- Fixed channel priority and round-robin channel arbitration

## 3.3 Architecture

In ESP32-H2, all modules that need high-speed data transfer support GDMA. The GDMA controller and CPU data bus have access to the same address space in internal RAM. Figure 3.3-1 shows the basic architecture of the GDMA controller.

Figure 3.3-1. GDMA controller Architecture

The GDMA controller has six independent channels, i.e., three transmit channels and three receive channels. Every channel can be connected to different peripherals. In other words, channels are general-purpose, shared by peripherals.

The GDMA controller reads data from or writes data to internal RAM via AHB_BUS. Before this, the GDMA controller uses a fixed-priority arbitration scheme for channels requesting read or write access. For the available address range of Internal RAM, please see Chapter 4 System and Memory.

Software can use the GDMA controller through linked lists. These linked lists, stored in internal RAM, consist of outlinkn and inlinkn, where n indicates the channel number (ranging from 0 to 2). The GDMA controller reads an outlinkn (i.e., a linked list of transmit descriptors) from internal RAM and transmits data in corresponding RAM according to the outlinkn, or reads an inlinkn (i.e., a linked list of receive descriptors) and stores received data into specific address space in RAM according to the inlinkn.
```