**Chapter Title:**
Chapter 26

**Subheading and Content:**

- **SDIO Slave Controller (SDIO)**
  
  The ESP32 features hardware support for the industry-standard Secure Digital (SD) device interface that conforms to the SD Input/Output (SDIO) Specification Version 2.0. This allows a host controller to access the ESP32 via an SDIO bus protocol, enabling high-speed data transfer.

- **Overview**
  
  The SDIO interface may be used to read ESP32 SDIO registers directly and access shared memory via Direct Memory Access (DMA), thus reducing processing overhead while maintaining high performance.
  
- **Features**

  - Meets SDIO V2.0 specification
  - Supports SDIO SPI, 1-bit, and 4-bit transfer modes
  - Full host clock range of 0 ~ 50 MHz
  - Configurable sample and drive clock edge
  - Integrated, SDIO-accessible registers for information interaction
  - Supports SDIO interrupt mechanism
  - Automatic data padding
  - Block size of up to 512 bytes
  - Interrupt vector between Host and Slave for bidirectional interrupt
  - Supports DMA for data transfer

- **Functional Description**

  The functional block diagram is shown in Figure 26.3-1.

**Subsection:**
SDIO Slave Block Diagram
  
The text mentions that the functional block diagram of the SDIO slave module can be found, but it does not provide a description or details about this figure directly within its content on the page.
  
**Footer Information:** 
Espressif Systems
ESP32 TRM (Version 5.6)