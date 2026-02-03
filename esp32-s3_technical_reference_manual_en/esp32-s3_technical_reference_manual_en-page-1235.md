**Title: Chapter 32 USB On-The-Go (USB)**

---

**Figure Caption:**  
*Figure 32.3-6. Scatter/Gather DMA Descriptor List*

**Diagram Description in the Image:**
- Data Descriptor Pointer pointing to Buffer Status Quadlet.
- Buffer Status Quadlet connected with Buffer Pointer leading towards a Buffer.

---

**Body Text and Subsections**

**Section Title (Subheading):**  
*32.3.6 Transaction and Transfer Level Operation*

When operating in either Host or Device mode, communication can operate either at the transaction level or the transfer level.

**Subsection Title:**  
*32.3.6.1 Transaction and Transfer Level in DMA Mode*

When operating at the transfer level in DMA Host mode, software is interrupted only when a channel has been halted. Channels are halted when their programmed transfer size has completed successfully, has received a STALL, or if there are excessive transaction errors (i.e., 3 consecutive transaction errors). When operating in DMA Device mode, all errors are handled by the controller core itself.

When operating at the transaction level in DMA mode, the transfer size is set to the size of one data packet (either a maximum packet size or a short packet size).

**Subsection Title:**  
*32.3.6.2 Transaction and Transfer Level in Slave Mode*

When operating at the transaction level in Slave Mode, transfers are handled on one transaction at a time. Each data payload should correspond to a single data packet, and software must determine whether a retry of the transaction is necessary based on the handshake response received on the USB (e.g., ACK or NAK).

The following table describes transaction-level operation in Slave mode for both IN and OUT transactions.

---

**Footer:**
- Espressif Systems
- Submit Documentation Feedback

**Document Version:**  
ESP32-S3 TRM (Version 1.7)