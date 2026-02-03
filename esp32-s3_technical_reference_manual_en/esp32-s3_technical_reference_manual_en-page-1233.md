**Chapter Title:**
Chapter 32 USB On-The-Go (USB)

**Section Titles and Content:**

### 32.3.4 Interrupt Hierarchy

OTG_FS provides a single interrupt line which can be routed via the interrupt matrix to one of the CPUs. The interrupt signal can be unmasked by setting USB_GLBLINTRMSK. The OTG_FS interrupt is an OR of all bits in the USB_GINTSTS_REG register, and the bits in USB_GINTSTS_REG can be unmasked by setting the corresponding bits in the USB_GINTMSK_REG register. USB_GINTSTS_REG contains system level interrupts, and also specific bits for Host or Device mode interrupts, and OTG specific interrupts. OTG_FS interrupt sources are organized as Figure 32.3-5 shows.

The following bits of the USB_GINTSTS_REG register indicate an interrupt source lower in the hierarchy:

- **USB_PRTINT**: indicates that the Host port has a pending interrupt.
- **USB_HCHINT**: indicates that one or more Host channels have a pending interrupt. Read the USB_HAINT_REG register to determine which channel(s) have a pending interrupt, then read the pending channel's USB_HCNInn'REG register to determine the interrupt source.

- **USB_OEPINT**: indicates that one or more OUT endpoints have a pending interrupt.
  - Read the USB_DAINT_REG register to determine which OUT endpoint(s) have a pending interrupt,
  - Then read the USB_DOEPInnn'REG register to determine the interrupt source

- **USB_IEPINT**: indicates that one or more IN endpoints have a pending interrupt. 
  - Read the USB_DAINT_REG register to determine which IN endpoint(s) are pending, then
  - Read the pending IN endpoint's USB_DIEPInnn'REG register to determine the interrupt source.

- **USB_OTGINT**: indicates an On-The-Go event has triggered an interrupt.
  - Read the USB_GOTGINT_REG register to determine which OTG event(s) triggered the interrupt

### 32.3.5 DMA Modes and Slave Mode

USB On-The-Go supports three ways to access memory: Scatter/Gather DMA mode, Buffer DMA mode, and Slave mode.

#### Subsection Title:
**32.3.5.1 Slave Mode**

When operating in Slave mode, all data payloads must be pushed/popped to and from the FIFOs by the CPU:

- When transmitting a packet using IN endpoints or OUT channels,
  - The data payload must be pushed into
  - Corresponding endpoint or channel's TX FIFO.

- When receiving a packet:
  - The packet’s status entry must first be popped off the RX FIFO.
  - By reading USB_GRXSTSP_REG. 
  - The status entry should be used to determine the length of the packet’s payload (in bytes).
  - The corresponding number of bytes
    - Must then be manually popped off the RX FIFO by reading from the RX FIFO's memory region.

#### Subsection Title:
**32.3.5.2 Buffer DMA Mode**

Buffer mode is similar to Slave mode but utilizes the internal DMA to push and pop data payloads to the FIFOs

**Footer:**
Espressif Systems
1233 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback