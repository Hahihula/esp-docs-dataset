**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Section Titles and Content:**

- **25.5.3 Data Overrun Interrupt (DOI)**
  - The Data Overrun Interrupt (DOI) is triggered when the message being read is overrun and invalid.
  - Description of conditions for DOI:
    - If TWAI_ERR_ST = 1 and TWAI_BUS_OFF_ST = 0: The TEC or REC error counters have exceeded the threshold value set by TWAI_ERR_WARNING_LIMIT_REG.
    - If TWAI_ERR_ST = 1 and TWAI BUS OFF ST = 1: The TWAI controller has entered the BUS_OFF state (due to the TEC >=256).
    - If TWAI_ERR_ST = 0 and TWAI BUS OFF ST = 1: The TWAI controller’s TEC has dropped below the threshold value set by TWAI_ERR_WARNING_LIMIT_REG during BUS OFFSET recovery.

- **25.5.3.5 Error Passive Interrupt (TXI)**
  - Description of conditions for TXI:
    - The Error Passive Interrupt (EPI) is triggered whenever the TWAI controller transitions from Error Active to Error Passive, or vice versa.
  
- **25.5.3.6 Arbitration Lost Interrupt (ALI)**
  - Description: 
    - The Arbitration Lost Interrupt (ALI) is triggered when the TWAI controller fails attempting to transmit a message and loses arbitration.

- **25.5.3.7 Bus Error Interrupt (BEI)**
  - Description:
    - When an error occurs on the TWAI bus, BEI triggers.
    - The Bus Error type bit position in the Error Code Capture register is automatically recorded when BEI happens again; however, it will not record new information until cleared via a read from the CPU.

- **25.5.4 Transmit and Receive Buffers**
  - Overview of Buffers

**Table:**

| TWAI address | Content       | TWAI address | Content      |
|--------------|---------------|--------------|--------------|
| TX/RX frame information | 0x40 | TX/RX frame information | 0x40 |
| TX/RX identifier 1 | 0x44 | TX/RX identifier 1 | 0x44 |
| TX/RX identifier 2 | 0x48 | TX/RX identifier 2 | 0x48 |
| TX/RX data byte 1 | 0x4c | TX/RX identifier 3 | 0x4c |

**Footer:**
Espressif Systems
540 ESP32 TRM (Version 5.6)
Submit Documentation Feedback