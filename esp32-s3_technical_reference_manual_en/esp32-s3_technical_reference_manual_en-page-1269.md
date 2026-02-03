**Chapter Title:**
Chapter 34

**Section Heading:**
SD/MMC Host Controller (SDHOST)

**Subsection 1: Overview**

The ESP32-S3 memory card interface controller provides a hardware interface between the Advanced Peripheral Bus (APB) and an external memory device. The memory card interface allows the ESP32-S3 to be connected to SDIO memory cards, MMC cards and devices with a CE-ATA interface. It supports two external cards (Card0 and Card1). And all SD/MMC module interface signals only connect to GPIO pad by GPIO matrix.

**Subsection 2: Features**

This module supports the following features:

- Two external cards
- SD Memory Card standard: V3.0 and V3.01
- MMC: V4.41, V4.5, and V4.51
- CE-ATA: V1.1
- 1-bit, 4-bit, and 8-bit modes

The SD/MMC controller topology is shown in Figure 34.2-1.

**Figure Description (Figure Caption):**
Figure 34.2-1. SD/MMC Controller Topology

**Diagram Details:**

- **Host Controller:** Central component with connections to Card0 and Card1.
- Connections from Host Controller:
  - To "SD Mem" on the left, labeled as "Data width 1/4 bits".
  - To "Card0", which is connected further down to components like SDIO, MMC, CE-ATA (labeled Data width 1/4 bits).
  - Similarly for Card1.
  
**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:** 
ESP32-S3 TRM (Version 1.7)