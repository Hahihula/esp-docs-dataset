**Title: Functional Description**

---

### Alignment:

- **GDMA-AHB:**
  * Descriptor address: 1-word aligned

* Data address and length:
  - Internal memory and non-encrypted external memory address space: no requirements
  - Encrypted external memory address space: 16-byte aligned

- **GDMA-AXI:**
  * Descriptor address: 2-word aligned

* Data address and length:
  - Internal memory and non-encrypted external memory address space: no requirements
  - Encrypted external memory address space: 16-byte aligned

- Linked list of descriptors
- INCR burst transfer when accessing memory
- Three transmit channels and three receive channels for each controller
- Software-configurable selection of peripheral requesting its service
- Configurable channel priority and weight arbitration
- Support for memory transfer
- CRC calculation of data

---

### 4.1.2.2 VDMA Controller (VDMA)

**Body Text:**
DMA (Direct Memory Access) enables direct access to system memory or peripherals without CPU involvement. The VDMA controller on ESP32-P4 is a general-purpose DMA that performs high-speed data transfer from memory to memory, from memory to peripheral, and from peripheral to memory. The VDMA complies with the AXI3 protocol and includes two AXI master interfaces. This design allows users to select between the two interfaces for data transfer dynamically.

**Feature List:**
- Four channels for unidirectional data transfer from source to destination
- Two AXI master interfaces
- Handshake with MIPI DSI (Display Serial Interface) and ISP (Image Signal Processor)
- Memory-to-memory, ISP-to-memory, and MIPI DSI-to-memory transfer types
- Multiple levels of DMA transfer hierarchy
- Configurable transfer type, transfer length, and transfer size for each channel
- Single-block transfer

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
ESP32-P4 Series Datasheet v0.6