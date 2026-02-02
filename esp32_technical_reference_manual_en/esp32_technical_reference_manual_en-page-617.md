**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Navigation Link:**
GoBack

---

**Section Heading:**
Register 27.11. CMD_REG (0x002C)

**Continuation Note:**
Continued from the previous page...

**Subsection with Code and Description:**
- **UPDATE_CLOCKRegisters_ONLY (R/W)**
  - **Description:** 
    O: Normal command sequence.
    1: Do not send commands, just update clock register value into card clock domain
    Following register values are transferred into card clock domain: CLKDIV, CLRSRC, and CLKENA. Changes card clocks (change frequency, truncate off or on, and set low-frequency mode). This is provided in order to change clock frequency or stop clock without having to send command to cards.
  - **Additional Information:** 
    During normal command sequence, when update_clock_registers_only = O, following control registers are transferred from BIU to CIU: CMD, CMDARG, TMOUT, CTTYPE, BLKSIZ, and BYTCNT. CIU uses new register values for new command sequence to card(s). When bit is set, there are no Command Done interrupts because no command is sent to SD/MMC/CEATA cards.

**Subsection with Code and Description:**
- **CARD_NUMBER (R/W)**
  - **Description:** 
    Card number in use. Represents physical slot number of card being accessed. In MMC-Ver3.3-only mode, up to two cards are supported. In SD-only mode, up to two cards are supported.
  
**Subsection with Code and Description:**
- **SEND_INITIALIZATION (R/W)**
  - **Description:** 
    O: Do not send initialization sequence (80 clocks of 1) before sending this command.
    1: Send initialization sequence before sending this command.

**Subsection with Code and Description:**
- **STOP_ABORT_CMD (R/W)**
  - **Description:** 
    O: Neither stop nor abort command can stop current data transfer. If abort is sent to function-number currently selected or not in data-transfer mode, then bit should be set to 0.
    1: Stop or abort command intended to stop current data transfer in progress. When open-ended or predefined data transfer is in progress, and host issues stop or abort command to stop data transfer, bit should be set so that command/data state-machines of CIU can return correctly to idle state.

**Subsection with Code and Description:**
- **WAIT_PRVDATA_COMPLETE (R/W)**
  - **Description:** 
    O: Send command at once, even if previous data transfer has not completed;
    1: Wait for previous data transfer to complete before sending Command.
    The wait_prvdata_complete = 0 option is typically used to query status of card during data transfer or to stop current data transfer. card_number should be same as in previous command.

**Subsection with Code and Description:**
- **SEND_AUTO_STOP (R/W)**
  - **Description:** 
    O: No stop command is sent at the end of data transfer;
    1: Send stop command at the end of data transfer.
  
**Continuation Note:**
Continued on the next page...

---

**Footer Information:**
Espressif Systems
617 ESP32 TRM (Version 5.6)
Submit Documentation Feedback