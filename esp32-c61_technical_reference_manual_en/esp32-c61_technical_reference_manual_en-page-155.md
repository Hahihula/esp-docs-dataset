

```markdown
- Data address and length: no requirements
• Linked list of descriptors
• INCR burst transfer when accessing memory
• Two transmit channels and two receive channels
• Software-configurable selection of peripheral requesting its service
• Configurable channel priority and weight arbitration
• Support for memory transfer
```

## 3.3 Architecture

In ESP32-C61, all modules that need high-speed data transfer support GDMA. The GDMA controller and CPU data bus have access to the same address space in memory. Figure 3.3-1 shows the basic architecture of the GDMA controller.

Figure 3.3-1. GDMA controller Architecture

GDMA has four independent channels: two transmit channels and two receive channels. Every channel can be connected to different peripherals. In other words, channels are general-purpose, and shared by peripherals.

GDMA reads data from or writes data to memory via AHB_BUS. Before this, GDMA uses configurable arbitration schemes for channels requesting read or write access. For the available address range of internal and external memory, please see Chapter 4 System and Memory.

Software can use the GDMA through linked lists, which are stored in the internal memory. These linked lists consist of outlinkn and inlinkn, where n indicates the channel number (ranging from 0 to 1). The GDMA reads an outlinkn (i.e., a linked list of transmit descriptors) from memory and transmits data in the corresponding memory according to the outlinkn, or reads an inlinkn (i.e., a linked list of receive descriptors) and stores received data into specific address space in the memory according to the inlinkn.
```