**Title:**
Chapter 26 SDIO Slave Controller (SDIO)

**Diagram Description:**
Figure 26.3-5 illustrates a linked list of descriptors and data buffers in the context of an SDIO slave controller.

**Subheading:**
26.3.5 Packet-Sending/-Receiving Procedure

**Body Text:**
The SDIO Host and Slave devices need to follow specific data transfer procedures to successfully exchange data over the SDIO interface.

**Sub-subheading:**
26.3.5.1 Sending Packets to SDIO Host

**Body Text:**
The transmission of packets from Slave to Host is initiated by the Slave. The Host will be notified with an interrupt (for detailed information on interrupts, please refer to SDIO protocol). After the Host reads the relevant information from the Slave, it will initiate an SDIO bus transaction accordingly. The whole procedure is illustrated in Figure 26.3-6.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version:**
566 ESP32 TRM (Version 5.6)