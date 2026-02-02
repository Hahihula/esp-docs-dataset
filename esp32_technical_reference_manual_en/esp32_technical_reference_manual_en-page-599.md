**Title: Chapter 27 SD/MMC Host Controller (SDHOST)**

---

**Figure Caption:**  
*Figure 27.4-1. SDIO Host Block Diagram*

---

### Section Title:
#### **27.4.1 BIU**

The BIU provides the access to registers and FIFO data through the Host Interface Unit (HIU). Additionally, it provides FIFO access to independent data through a DMA interface. The host interface can be configured as an APB interface. Figure 27.4-1 illustrates the internal components of the BIU. The BIU provides the following functions:

- Host interface
- DMA interface
- Interrupt control
- Register access
- FIFO access
- Power/pull-up control and card detection

---

### Section Title:
#### **27.4.1.2 CIU**

The CIU module implements the card-specific protocols. Within the CIU, the command path control unit and data path control unit prompt the controller to interface with the command and data ports, respectively, of the SD/MMC/CE-ATA cards. The CIU also provides clock control. Figure 27.4-1 illustrates the internal structure of the CIU, which consists of the following primary functional blocks:

- Command path
- Data path
- SDIO interrupt control
- Clock control
- Mux/demux unit

---

### Section Title:
#### **27.4.2 Command Path**

The command path performs the following functions: 

[End of visible text]