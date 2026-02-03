**Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Figure Title and Description:**
- **Figure 31.3-1. Bit Fields in Data Frames and Remote Frames**

**Body Text with Descriptions of CRC Field, ACK Field, and Table Content:**

The CRC field primarily consists of a CRC sequence. The CRC sequence is a 15-bit cyclic redundancy code calculated from the de-stuffed contents (everything from the SOF to the end of the data field) of a data or remote frame.

**ACK Field**
The ACK field primarily consists of an ACK Slot and an ACK Delim. The ACK field is mainly intended for the receiver to indicate to a transmitter that it has received an effective message.

**Table 31.3-1. Data Frames and Remote Frames in SFF and EFF**

| **Data/Remote Frames** | **Description** |
|------------------------|------------------|
| SOF (Start of Frame)   | The SOF is a single dominant bit used to synchronize nodes on the bus. |
| Base ID                | The Base ID (ID.28 to ID.18) is the 11-bit identifier for SFF, or the first 11-bits of the 29-bit identifier for EFF. |
| RTR                    | The RTR (Remote Transmission Request) bit indicates whether the message is a data frame (dominant) or a remote frame (recessive). This means that a remote frame will always lose arbitration to a data frame given they have the same ID. |
| SRR                    | The SRR (Substitute Remote Request) bit is transmitted in EFF to substitute for the RTR bit at the same position in SFF. |

**Footer:**
Espressif Systems
1188 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Navigation Link:** 
GoBack