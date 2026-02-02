**Title: Chapter 27 SD/MMC Host Controller (SDHOST)**

---

### Figure Description:
- **Figure Caption:** The Structure of a Linked List  
- **Figure Reference:** Table 27.8-1.

### Text Content:

#### Section Title:
The DESO element contains control and status information.
**Table 27.8-1. DESO**

| Bits | Name       | Description                                                                 |
|------|------------|-----------------------------------------------------------------------------|
| 31   | OWN        | When set, this bit indicates that the descriptor is owned by the DMAC. When reset, it indicates that the descriptor is owned by the Host. The DMAC clears this bit when it completes the data transfer. |
|      |           | These error bits indicate the status of the transition to or from the card. |
| 30   | CES (Card Error Summary) | Indicates their digital logic OR gate.                                      |
|      |           | - EBE: End Bit Error                                                       |
|      |           | - RTO: Response Time out                                                   |
|      |           | - RCRC: Response CRC                                                       |
|      |           | - SBE: Start Bit Error                                                     |
| 29:6| Reserved   |                                                                             |
| 5    | ER (End of Ring) | When set, this bit indicates that the descriptor list has reached its final descriptor. The DMAC then returns to the base address of the list, creating a Descriptor Ring. |
| 4    | CH (Second Address Chained) | When set, this bit indicates that the second address in the descriptor is the Next Descriptor address. When this bit is set, BS2 (DES1[25:13]) should be all zeros. |
| 3    | FD (First Descriptor)   | When set, this bit indicates that this descriptor contains the first buffer of data. If the size of the first buffer is zero, the Next Descriptor contains beginning of the data. |

---

**Footer Information:**  
Espressif Systems  
604  
Submit Documentation Feedback  
ESP32 TRM (Version 5.6)