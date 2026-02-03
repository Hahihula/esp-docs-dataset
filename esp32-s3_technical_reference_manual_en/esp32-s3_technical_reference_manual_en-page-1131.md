**Title: Chapter 30 SPI Controller (SPI)**

---

### Diagrams and Descriptions:

- **Figure 30.5-7**: Connection of GP-SPI2 to Flash and External RAM in 4-bit Mode.
  - The diagram shows the connections between Master components such as FSPID, FSPIQ, FSPIWP, FSMIHD, FSMICLK, FSMICS0 with Slave components like SI (flash), SO, WP, HOLD, SCK, CE. GP-SPI2 is also connected to these lines.

- **Figure 30.5-8**: SPI Quad I/O Read Command Sequence Sent by GP-SPI2 to Flash.
  - The diagram illustrates the command sequence with phases labeled as "Command phase," "Address phase" (with dummy bits), and "Data phase."

---

### Section: DMA-Controlled Configurable Segmented Transfer

**Subtitle:** **30.5.8.5**

- Note:
  - This feature is only supported by GP-SPI2.
  - There's no separate section on how to configure a single transfer in master mode, as the CONF state of a configurable segmented transfer can be skipped for this purpose.

---

### Introduction

When GP-SPI2 works as a master, it provides a feature named: configurable segmented transfer controlled by DMA. A DMA-controlled transfer in master mode can consist:
- Of only one transaction.
- Or a configurable segmented transfer consisting of several transactions (segments).

---

**Footer:**  
Espressif Systems  
1131  
ESP32-S3 TRM (Version 1.7)  

Submit Documentation Feedback

[GoBack](#)