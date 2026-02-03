**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Section Titles and Subsections with Content:**

1. **PDM RX mode**
   - In this mode, pulse density modulation (PDM) data is received and stored into memory via DMA.
   - The signal lines include:
     - WS
     - DATA

2. **TDM TX mode**
   - TDM standard supported in the way of time division multiplexing (TDM).
   - Data up to 16 channels can be sent.

3. **PDM TX mode**
   - Pulse density modulation data is sent from memory via DMA.
   - The signal lines include:
     - WS
     - DATA

4. **PCM-to-PDM TX mode** 
   - I2SO as a master converts the pulse code modulated (PCM) data to PDM and sends it out.

5. **PDM-to-PCM RX mode**
   - Pulse density modulation is received, converted into PCM.
   - The signal lines include:
     - WS
     - DATA

**Subsection Title: 28.3 Features**

**Body Text under Subsection "Features":**
I2Sn has the following features:

- Master mode and slave mode
- Full-duplex and half-duplex communications
- Separate TX unit and RX unit, independent of each other.
- TX unit and RX unit to work independently and simultaneously.

A variety of audio standards supported:
  - TDM Philips standard
  - TDM MSB alignment standard
  - TDM PCM standard

PDM mode is also mentioned as a feature. 

**List under "Various TX/RX modes supported":**
- PDM TX mode
- TDM RX mode

**Footer:**
Espressif Systems  
ESP32-S3 TRM (Version 1.7)