**Chapter Title:**
Chapter 28

**Section Heading:**
I2S Controller (I2S)

**Subsection 1: Overview**

**Body Text:**
ESP32-S3 has two built-in I2S interfaces (i.e., I2SO and I2ST), which provides a flexible communication interface for streaming digital data in multimedia applications, especially digital audio applications.

The I2S standard bus defines three signals: a bit clock signal (BCK), a channel/word select signal (WS), and a serial data signal (SD). A basic I2S data bus has one master and one slave. The roles remain unchanged throughout the communication. The I2S module on ESP32-S3 provides separate transmit (TX) and receive (RX) units for high performance.

**Note:**
The information provided in this chapter applies to both I2SO and I2ST. Unless otherwise indicated, I2Sn or I2S in this chapter refer to both I2SO and I2ST.

---

**Subsection 2: Terminology**

To better illustrate the functionality of I2Sn, the following terms are used:

- **Master mode**
  - As a master, I2Sn outputs BCK/WS signals, and sends data to or receives data from a slave.
  
- **Slave mode**
  - As a slave, I2Sn inputs BCK/WS signals, and receives data from or sends data to a master.

- **Full-duplex**
  - The sending line and receiving line between the master and the slave are independent. Sending data and receiving data happen at the same time.
  
- **Half-duplex**
  - Only one side, the master or the slave, sends data first, and the other side receives data. Sending data and receiving data cannot happen at the same time.

- **TDM RX mode**
  - In this mode, pulse code modulated (PCM) data is received and stored into memory via DMA in a way of time division multiplexing (TDM). The signal lines include: BCK, WS, and DATA. Data from 16 channels at most can be received. TDM Philips standard, TDM MSB alignment standard, TDM PCM standard are supported in this mode, depending on user configuration.

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)