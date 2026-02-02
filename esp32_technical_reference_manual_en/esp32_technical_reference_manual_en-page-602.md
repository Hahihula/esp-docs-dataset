**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Body Text:**

- During an open-ended card-write operation, if the card clock is stopped due to FIFO being empty, the software must fill FIFO with data first, and then start the card clock. Only then can it issue a stop/abort command to the card.

- During an SDIO/COMBO card transfer, if the card function is suspended and the software wants to resume the suspended transfer, it must first reset FIFO, and then issue the resume command as if it were a new data-transfer command.
  
- When issuing card reset commands (CMD0, CMD15 or CMD52_reset), while a card data transfer is in progress, the software must set the stop_abort_cmd bit in the Command register, so that the CIU can stop the data transfer after issuing the card reset command.

- When the data’s end bit error is set in the RINTSTS register, the CIU does not guarantee SDIO interrupts. In such a case, the software ignores SDIO interrupts and issues a stop/abort command to the card, so that the card stops sending read-data.
  
- If the card clock is stopped due to FIFO being full during a card read, the software will read at least two FIFO locations to restart the card clock.

- Only one CE-ATA device at a time can be selected for a command or data transfer. For example, when data are transferred from a CE-ATA device, a new command should not be sent to another CE-ATA device.
  
- If a CE-ATA device’s interrupts are enabled (nEN=0), a new RW_BLK command should not be sent to the same device if the execution of a RW_BLK command is already in progress (the RW_BLK command used in this databook is the RW_MULTIPLE_BLOCK MMC command defined by the CE-ATA specifications). Only the CCSD can be sent while waiting for the CCS.
  
- If, however, a CE-ATA device’s interrupts are disabled (nEN=1), a new command can be issued to the same device, allowing it to read status information.

- Open-ended transfers are not supported in CE-ATA devices.

- The send_auto_stop signal is not supported (software should not set the send_auto_stop bit) in CE-ATA transfers.

**List of Values that Cannot Be Changed Before a Command Has Been Issued:**

- CMD - command
- CMDARG - command argument
- BYTCNT - byte count
- BLKSIZ - block size
- CLKDIV - clock divider
- CKLENA - clock enable
- CLKSRC - clock source
- TMOUT - timeout
- CTYPE - card type

**Footer:**
Espressif Systems  
602 ESP32 TRM (Version 5.6)