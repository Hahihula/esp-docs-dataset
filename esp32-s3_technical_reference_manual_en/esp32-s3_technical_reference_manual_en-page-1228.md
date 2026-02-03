**Chapter Title:**
Chapter 32 USB On-The-Go (USB)

**Section Titles and Content:**

### **32.2.3 Host Mode Features**
- Eight channels (pipes)
  - A control pipe consists of two channels (IN and OUT), as IN and OUT transactions must be handled separately. Only Control transfer type is supported.
  - Each of the other seven channels is dynamically configurable to be IN or OUT, and supports Bulk, Isochronous, and Interrupt transfer types.

- All channels share an RX FIFO, non-periodic TX FIFO, and periodic TX FIFO. The size of each FIFO is configurable.

### **32.3 Functional Description**

#### 32.3.1 Controller Core and Interfaces

**Figure Title:**
Figure 32.3-1. OTG_FS System Architecture

**Diagram Labels (from left to right):**
- SPRAM
- Data FIFO RAM I/F
- USB Controller Core
- APB Interface CPU Interface
- Memory
- CPU
- USB External Controller
- USB1.1 FS Serial Transceiver

**Text:**

The core part of the OTG_FS peripheral is the USB Controller Core. The controller core has the following interfaces (see Figure 32.3-1):

- **CPU Interface**
  - Provides the CPU with read/write access to the controller core's various registers and FIFOs. This interface is internally implemented as an AHB Slave Interface. The way to access the FIFOs through the CPU interface is called Slave mode.

- **APB Interface**
  - Allows the CPU to control the USB controller core via the USB external controller.

- **DMA Interface**
  - Provides the controller core's internal DMA with read/write access to system memory (e.g., fetching and writing data payloads when operating in DMA mode). This interface is internally implemented as an AHB Master interface.

- **USB 1.1 Interface**
  - This interface is used to connect the controller core to a USB 1.1 FS serial transceiver. Aside from USB OTG, ESP32-S3 also includes a USB Serial/JTAG controller (see Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)). These two USB controllers can utilize the integrated internal transceiver by

**Footer:**
Espressif Systems
Submit Documentation Feedback