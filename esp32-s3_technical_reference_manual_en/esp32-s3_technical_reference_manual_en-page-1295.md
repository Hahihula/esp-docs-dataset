**Title: Chapter 34 SD/MMC Host Controller (SDHOST)**

**Subtitle: Register 34.18. SDHOST_STATUS_REG (0x0048)**

**Diagram Description**
- The diagram is a state machine with various states and transitions, labeled as follows:
  - **SDHOST_FIF0_COUNT**: FIFO count, number of filled locations in FIFO.
  - **SDHOST_RESPONSE_INDEX**: Index of previous response, including any auto-stop sent by core (RO).
  - **SDHOST_DATA_STATE_MC BUSY**: Data transmit or receive state-machine is busy. (RO)
  - **SDHOST_DATA BUSY**: Inverted version of raw selected sdhost_card_data[0].
    - Card data not busy.
    - Card data busy. (RO)
  - **SDHOST_DATA_3_STATUS**: Raw selected sdhost_card_data[3], checks whether card is present:
    - Card not present
    - Card present. (RO)

**Table: SDHOST_COMMAND_FSM_STATES**
- Command FSM states, listed as follows with corresponding actions for each state number from 0 to 15.
  - **0**: Idle;
  - **1**: Send init sequence;
  - **2**: Send cmd start bit;
  - **3**: Send cmd tx bit;
  - **4**: Send cmd index + arg;
  - **5**: Send cmd crc7;
  - **6**: Send cmd end bit;
  - **7**: Receive resp start bit;
  - **8**: Receive resp IRO response;
  - **9**: Receive resp tx bit;
  - **10**: Receive resp cmd idx;
  - **11**: Receive resp data;
  - **12**: Receive resp crc7;
  - **13**: Receive resp end bit;
  - **14**: Cmd path wait NCC;
  - **15**: Wait, cmd-to-response turnaround.

**Footer**
- "Continued on the next page..."
- Page number: 1295
- Document version and title information:
  - ESP32-S3 TRM (Version 1.7)
- Company name: Espressif Systems

**Navigation Links**
- Submit Documentation Feedback