

```markdown
Chapter 6 2D-DMA Controller (2D-DMA)

Figure 6.3-1. 2D-DMA Architecture

The 2D-DMA has seven independent channels: four transmit channels and three receive channels. Every channel can be connected to different peripherals, or in other words shared by peripherals.

The macroblock reordering and color space conversion features of the 2D-DMA are not supported by all channels. Among the channels, transmit channel 0 and receive channel 0 support macroblock reordering, while transmit channel 0 ~ 3 and receive channel 0 support color space conversion.

The 2D-DMA reads data from or writes data to the internal or external memory via AXI_BUS. Before the data transfer, the 2D-DMA uses configurable arbitration schemes for channels requesting read or write access. For the available address range of internal and external memory, please see Chapter 7 System and Memory.

The software can use the 2D-DMA through linked lists stored in internal or external memory. These linked lists consist of outlinkn and inlinkn, where n indicates the channel number. For outlinkn, n ranges from 0 to 3; for inlinkn, n ranges from 0 to 2. The 2D-DMA reads an outlinkn (i.e., a linked list of transmit descriptors) from memory and transmit data in corresponding memory according to the outlinkn, or read an inlinkn (i.e., a linked list of receive descriptors) and store received data into specific address space in memory according to the inlinkn.

6.4 Functional Description

6.4.1 Transfer Mode

The 2D-DMA supports four transfer modes:

*   1D mode: enabled by setting the 2DEN field of DWO and the mod field of DW2 to 0. In this mode, the 2D-DMA has the same functionalities as GDMA-AXI: it performs memory read/write operations based on the data length and memory space configured in the linked list, and the operation addresses are contiguous.
*   2D-MODO mode: enabled by setting the 2DEN field of DWO to 1 and the mod field of DW2 to 0. In this mode, the 2D-DMA reads or writes a hb*vb macroblock starting from the (X, Y) coordinates of the HA*VA image. After the last data in each row has been read or written, the address jumps to the address of the first data in the next row to be read or written.
```