

```markdown
Chapter 5

VDMA Controller (VDMA)

5.1 Overview

DMA (Direct Memory Access) enables direct access to system memory or peripherals without CPU involvement. The VDMA controller on ESP32-P4 is a general-purpose DMA that performs high-speed data transfer from memory to memory, from memory to peripheral, and from peripheral to memory. The VDMA complies with the AXI3 protocol and includes two AXI master interfaces. This design allows users to select between the two interfaces for data transfer dynamically.

5.2 Terminology

The following terms are defined in the context of the VDMA controller on ESP32-P4:

*   **AXI**: Advanced eXtensible Interface, a part of AMBA 3 (Advanced Microcontroller Bus Architecture) specification, designed to facilitate high bandwidth and low latency communication between memory and peripheral, and between memory and memory.
*   **Peripheral**: A system component that has a handshake interface with VDMA, as listed in Table 5.4-1.
*   **Memory**: A system component that is always ready for DMA transfer, which means there is no handshaking interface between VDMA and memory. The memory that supports VDMA data transfer includes HP L2MEM, external flash, and external RAM.
*   **Source**: Source memory or peripheral from which VDMA reads data via the AXI interface. VDMA then stores data in channel FIFO.
*   **Source transfer**: Transfer from the source to VDMA.
*   **Destination**: Destination peripheral or memory to which VDMA writes the data stored in channel FIFO.
*   **Destination transfer**: Transfer from VDMA to the destination.
*   **Channel**: Data path between source and destination.
*   **Master interface**: Refers to the two AXI master interfaces of VDMA.
*   **Slave interface**: The APB3 slave interface for programming registers.
*   **Handshaking interface**: The handshaking interface performs a handshake between VDMA and the source or destination peripheral. The handshaking interface requests, acknowledges, and controls an VDMA transfer.
*   **Flow controller**: The flow controller defines the length of a DMA block transfer and terminates the transfer. The flow controller can be VDMA, a source peripheral, or a destination peripheral, but it cannot be memory.
```