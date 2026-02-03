**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Section Titles and Content:**

### **31.5.3.3 Error Warning Interrupt (EWI)**

The Error Warning Interrupt (EWI) is triggered whenever there is a change to the TWAI_ERR_ST and TWAI_BUS_OFF_ST bits of the TWAI_STATUS_REG (i.e., transition from 0 to 1 or vice versa). Thus, an EWI could indicate one of the following events, depending on the values TWAI_ERR_ST and TWAI BUS OFF ST at the moment when the EWI is triggered.

- If TWAI_ERR_ST = 0 and TWAI BUS OFF ST = 0:
  - The TWAI controller was in the Error Active state; it indicates both the TEC and REC have returned below the threshold value set by TWAI ERR WARNING LIMIT REG.
  - If the TWAI controller was previously in the Bus Off Recovery state, it indicates that Bus Recovery has completed successfully.

- If TWAI_ERR_ST = 1 and TWAI BUS OFF ST = 0: The TEC or REC error counters have exceeded the threshold value set by TWAI ERR WARNING LIMIT REG.
- If TWAI_ERR_ST = 1 and TWAI BUS OFF ST = 1: The TWAI controller has entered the BUS OFF state (due to the TEC >= 256).
- If TWAI_ERR_ST = 0 and TWAI BUS OFF ST = 1: The TWAI controller's TEC has dropped below the threshold value set by TWAI ERR WARNING LIMIT REG during BUS recovery.

### **31.5.3.4 Data Overrun Interrupt (DOI)**

The Data Overrun Interrupt (DOI) is triggered whenever the Receive FIFO has overrun. The DOI indicates that the Receive FIFO is full and should be cleared immediately to prevent any further overrun messages.
The DOI is only triggered by the first message that causes the Receive FIFO to overrun (i.e., the transition from the Receive FIFO not being full to the Receive FIFO overflowing). Any subsequent overrun messages will not trigger the DOI again. The DOI could be triggered again when all received messages (valid or overrun) have been cleared.

### **31.5.3.5 Error Passive Interrupt (TXI)**

The Error Passive Interrupt (EPI) is triggered whenever the TWAI controller switches from Error Active to Error Passive, or vice versa.

### **31.5.3.6 Arbitration Lost Interrupt (ALI)**

The Arbitration Lost Interrupt (ALI) is triggered whenever the TWAI controller is attempting to transmit a message and loses arbitration. The bit position where the TWAI controller lost arbitration is automatically recorded in Arbitration Lost Capture register (TWAI_ARB LOST CAP REG). When the ALI occurs again, the Arbitration Lost Capture register will no longer record new bit location until it is cleared (via reading this register through the CPU).

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)