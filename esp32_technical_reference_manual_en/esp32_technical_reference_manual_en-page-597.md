**Title:**
Chapter 27

**Subtitle:**
SD/MMC Host Controller (SDHOST)

**Section Title:**
27.1 Overview

**Body Text:**
The ESP32 memory card interface controller provides a hardware interface between the Advanced Peripheral Bus (APB) and an external memory device. The memory card interface allows the ESP32 to be connected to SDIO memory cards, MMC cards and devices with a CE-ATA interface. It supports two external cards (Card0 and Card1).

**Section Title:**
27.2 Features

**Body Text:**
This module has the following features:

- Two external cards
- Supports SD Memory Card standard: versions 3.0 and 3.01
- Supports MMC: versions 4.41, 4.5, and 4.51
- Supports CE-ATA: version 1.1
- Supports 1-bit, 4-bit, and 8-bit (Card0 only) modes

The SD/MMC controller topology is shown in Figure **27.2-1**.

**Figure Caption:**
Figure 27.2-1. SD/MMC Controller Topology

**Diagram Description:**
A diagram showing the connection between a Host Controller and two cards, Card0 and Card1. Data width for each card (Card0 and Card1) is indicated as "Data width 1/4 bits".

**Footer Information:**
Espressif Systems
597 ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Navigation Link:**
GoBack