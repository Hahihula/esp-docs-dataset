**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Section Heading and Subheading with Content:**

- **Subsection:** Continued from the previous page...
  
  - **Title:** SDHOST_UPDATE_CLOCK_REGISTERS_ONLY
  
    - **Description:** 
      - "0: Normal command sequence; 1: Do not send commands, just update clock register value into card clock domain. (R/W)"
      
      - Following register values are transferred into card clock domain:
        - CLKDIV
        - CLRSRC
        - CLKENA
        
      - Changes card clocks (change frequency, truncate off or on, and set low-frequency mode). This is provided in order to change clock frequency or stop clock without having to send command to cards.
        
      - During normal command sequence, when sdhost_update_clock_registers_only = 0, following control registers are transferred from BIU to CIU: CMD, CMDARG, TMOUT, CTYP, BLKSIZ, and BYTCNT. CIU uses new register values for new command sequence to card(s). When bit is set, there are no Command Done interrupts because no command is sent to SD_MMC_CEATA cards.

- **Title:** SDHOST_CARD_NUMBER
  
  - "Card number in use. Represents physical slot number of card being accessed. In SD-only mode, up to two cards are supported. (R/W)"

- **Title:** SDHOST_SEND_INITIALIZATION
  
  - "0: Do not send initialization sequence (80 clocks of 1) before sending this command; 1: Send initialization sequence before sending this command. (R/W)"
  
  - After powered on, 80 clocks must be sent to card for initialization before sending any commands to card. Bit should set while sending first command to card so that controller will initialize clocks before sending command to card.

- **Title:** SDHOST_STOP_ABORT_CM
  
  - "0: Neither stop nor abort command can stop current data transfer. If abort is sent to function-number currently selected or not in data-transfer mode, then bit should be set to 0; 1: Stop or abort command intended to stop current data transfer in progress. (R/W)"
  
  - When open-ended or predefined data transfer is in progress, and host issues stop or abort command to stop data transfer, but should also that command/data state-machines of CIU can return correctly to idle state.

- **Title:** SDHOST_WAIT_PRVDATA COMPLETE
  
  - "0: Send command at once, even if previous data transfer has not completed; 1: Wait for previous data transfer to complete before sending Command. (R/W)"
  
  - The SDHOST WAIT PRVDATA COMPLETE[ ] option is typically used to query status of card during data transfer or to stop current data transfer. SDHOST_CARD_NUMBER should be same as in previous command.

- **Title:** SDHOST_SEND_AUTO_STOP
  
  - "0: No stop command is sent at the end of data transfer; 1: Send stop command at the end of data transfer. (R/W)"

**Footer Note:**
Continued on the next page...

**Document Footer Information:**
Espressif Systems
Page number: 1291
Document version and type information:
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback