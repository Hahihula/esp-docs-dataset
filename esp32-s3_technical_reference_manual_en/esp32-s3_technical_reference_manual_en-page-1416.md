**Chapter Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Section Titles and Subsections with Content:**

- **37.3 Functional Description**
  - **37.3.1 Architecture**
    - Diagram labeled "Figure 37.3-1 RMT Architecture" showing various components such as RAM, block0 to block4, Clock, FSM (Finite State Machine), Transmitter, Receiver etc.

- **37.3.2 RAM**

**Body Text:**
As shown in Figure 37.3-1, each TX channel (SEND_CHn) has:
- 1 x clock divider counter (Div Counter)
- 1 x state machine (FSM)
- 1 x transmitter

Each RX channel (RECV_CHm) has:
- 1 x clock divider counter (Div Counter)
- 1 x state machine (FSM)
- 1 x receiver

The eight channels share a 384 x 32-bit RAM.

**Footer:**
Espressif Systems
Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)