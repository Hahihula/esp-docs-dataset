**Title: Chapter 25 Two-Wire Automotive Interface (TWAI)**

---

### Figure Caption:
- **Figure 253-1:** The bit fields of Data Frames and Remote Frames.

### Text Content:

#### CRC Field Description:
The CRC Field primarily consists of a CRC Sequence. The CRC Sequence is a 15-bit cyclic redundancy code calculated from the de-stuffed contents (everything from the SOF to the end of the Data Field) of a Data or Remote Frame.

#### ACK Field Description:
The ACK Field primarily consists of an ACK Slot and an ACK Delim. The ACK Field is mainly intended for the receiver to send a message to a transmitter, indicating it has received an effective message.

---

### Table 253-1: Data Frames and Remote Frames in SFF and EFF

| **Data/Remote Frames** | **Description**
|------------------------|------------------------------------------------------------
| SOF                    | The SOF (Start of Frame) is a single Dominant bit used to synchronize nodes on the bus.
| Base ID                | The Base ID (ID.28 to ID.18) is the 11-bit Identifier for SFF, or the first 11-bits of the 29-bit Identifier for EFF.
| RTR                    | The RTR (Remote Transmission Request) bit indicates whether the message is a Data Frame (Dominant) or a Remote Frame (Recessive). This means that a Remote Frame will always lose arbitration to a Data Frame given they have the same ID.
| SRR                    | The SRR (Substitute Remote Request) bit is transmitted in EFF to substitute for the RTR bit at the same position in SFF.

---

### Footer:
- **Espressif Systems**
- Page number: 528
- Document version and submission information: ESP32 TRM (Version 5.6), Submit Documentation Feedback