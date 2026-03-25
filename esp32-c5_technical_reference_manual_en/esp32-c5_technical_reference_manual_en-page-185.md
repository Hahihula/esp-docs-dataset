

```markdown
- Descriptor address: 1-word aligned
- Data address and length: no requirements
- Linked list of descriptors
- INCR burst transfer when accessing memory
- Three transmit channels and three receive channels
- Software-configurable selection of peripheral requesting its service
- Configurable channel priority and weight arbitration
- Support for memory transfer

## 5.3 Architecture

In ESP32-C5, all modules that need high-speed data transfer support GDMA. The GDMA controller and CPU data bus have access to the same address space in memory. Figure 5.3-1 shows the basic architecture of the GDMA controller.

![Figure 5.3-1. GDMA controller Architecture](image_path)

GDMA has six independent channels: three transmit channels and three receive channels. Every channel can be connected to different peripherals. In other words, channels are general-purpose, and shared by peripherals.

GDMA reads data from or writes data to memory via AHB_BUS. Before this, GDMA uses configurable arbitration schemes for channels requesting read or write access. For the available address range of internal and external memory, please see Chapter 6 System and Memory.

Software can use the GDMA through linked lists, which are stored in the internal memory. These linked lists consist of outlinkn and inlinkn, where n indicates the channel number (ranging from 0 to 2). The GDMA reads
```