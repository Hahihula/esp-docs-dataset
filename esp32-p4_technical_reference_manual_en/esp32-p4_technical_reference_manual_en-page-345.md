

# 5.3 Features

VDMA supports the following features:

* Four channels for unidirectional data transfer from source to destination
* Two AXI master interfaces
* Handshake with MIPI DSI (Display Serial Interface) and ISP (Image Signal Processor)
* Memory-to-memory, ISP-to-memory, and MIPI DSI-to-memory transfer types
* Multiple levels of DMA transfer hierarchy
* Configurable transfer type, transfer length, and transfer size for each channel
* Single-block transfer
* Multi-block transfer based on contiguous address, automatic reloading register configuration, shadow registers, and linked lists
* Independent configuration of multi-block transfer type for source transfer and destination transfer
* Channel disabling without data loss
* Channel suspension, resume, and abortion
* Configurable priorities among arbitration channels
* Flow control using VDMA or peripherals
* Programmable mapping between peripherals and channels

## 5.4 Architectural Overview

Figure 5.4-1 shows the architecture of VDMA and its connection with other system components.