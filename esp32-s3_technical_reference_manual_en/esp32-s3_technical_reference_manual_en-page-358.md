**Chapter Title:**
Chapter 3 GDMA Controller (GDMA)

**Body Text:**

- Programmable length of data to be transferred in bytes
- Linked list of descriptors
- INCR burst transfer when accessing internal RAM
- Access to an address space of 480 KB at most in internal RAM
- Access to an address spacee of 32 MB at most in external RAM
- Five transmit channels and five receive channels
- Access to internal and external RAM supported by every channel
- Software-configurable selection of peripheral requesting its service supported by every channel
- Fixed channel priority and round-robin channel arbitration

**Subsection Title:**
3.3 Architecture

**Body Text:**

In ESP32-S3, all modules that need high-speed data transfer support GDMA. The GDMA controller and CPU data bus have access to the same address space in internal and external RAM. Figure 3.3-1 shows the basic architecture of the GDMA engine.

The GDMA controller has ten independent channels, i.e., five transmit channels and five receive channels. Every channel can be connected to different peripherals. In other words, channels are general-purpose shared by peripherals.

The GDMA engine has two independent AHB bus referred to as AHB_BUS1 and AHB BUS2 respectively. AHB BUS1 is used to read data from or write data to internal RAM, whereas AHB BUS2 is used to read data from or write data to external RAM. Before this, the GDMA controller uses fixed-priority arbitration scheme for channels requesting read or write access. For available address range of RAM, please see Chapter 4 System and Memory.

Software can use the GDMA engine through linked lists. These linked lists, stored in internal RAM, consist of outlinkn and inlinkn, where n indicates the channel number (ranging from 0 to 4). The GDMA controller reads an outlinkn (i.e., a linked list of transmit descriptors) from internal RAM and transmits data in corresponding

**Figure Caption:**
Figure 3.3-1. GDMA Engine Architecture