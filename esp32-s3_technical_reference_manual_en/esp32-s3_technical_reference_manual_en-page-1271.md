**Title: Chapter 34 SD/MMC Host Controller (SDHOST)**

---

### Figure Caption:
- **Figure 34.4-1. SDIO Host Block Diagram**

---

#### Section Title and Subtitle:

**34.4.1 Bus Interface Unit (BIU)**
- The BIU provides the access to registers and RAM data through the Host Interface Unit (HIU). Additionally, it provides a method to access memory data through a DMA interface. Figure 34.4-1 illustrates the internal components of the BIU. Figure **34.10-1** illustrates the clock selection. The BIU provides the following functions:
  - Host interface
  - DMA interface
  - Interrupt control
  - Register access
  - FIFO access
  - Power/pull-up control and card detection

---

**34.4.2 Command Path**
- The command path performs the following functions:

---

#### Section Title: 
**34.4.1.2 Card Interface Unit (CIU)**

- **The CIU module implements the card-specific protocols. Within the CIU, the command path control unit and data path control unit are used to interface with the command and data ports, respectively, of the SD/MMC/CE-ATA cards. The CIU also provides clock control. Figure 34.4-1 illustrates the internal structure of the CIU, which consists of the following primary functional blocks:**
  - Command path
  - Data path
  - SDIO interrupt control
  - Clock control
  - Mux/De-Mux unit

---

**Footer Information:**  
Espressif Systems  
ESP32-S3 TRM (Version 1.7)  

**Navigation Links:**  
- Submit Documentation Feedback