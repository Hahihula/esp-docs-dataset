**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Body Text:**

- During an open-ended card-write operation, if the card clock is stopped due to RAM being empty, the software must fill RAM with data first, and then start the card clock. Only then can it issue a stop/abort command to the card.

- During an SDIO/Combo card transfer, if the card function is suspended and the software wants to resume the suspended transfer, it must first reset RAM, setting SDHOST_FIFO_RESET bits and then issue the resume command as if it were a new data-transfer command.
  
- When issuing card reset commands (CMD0, CMD15 or CMD52_reset), while a card data transfer is in progress, the software must set the SDHOST_STOP_ABORT_CMD bit in SDHOST_CMD_REG register, so that the CIU can stop the data transfer after issuing the card reset command.

- When the data’s end bit error is set in the SDHOST_RINTSTS_REG register, the CIU does not guarantee SDIO interrupts. In such a case, the software ignores SDIO interrupts and issues a stop/abort command to the card, so that the card stops sending read-data.
  
- If the card clock is stopped due to RAM being full during a card read, the software will read at least two RAM locations to restart the card clock.

- Only one CE-ATA device at a time can be selected for a command or data transfer. For example, when data are transferred from a CE-ATA device, a new command should not be sent to another CE-ATA device.
  
- If a CE-ATA device’s interrupts are enabled (nIEN=0), a new SDHOST_RW_BLK command should not be sent to the same device if the execution of a SDHODT_RW_BLK command is already in progress. Only then can data transfers from that specific device continue.

- However, if however, a CE-ATA device’s interrupts are disabled (nIEN=1), a new command can still issue and read status information.
  
- Open-ended transfers are not supported in CE-ATA devices
  
- The sdhost_send_auto_stop signal is not supported (software should set the sdhost_send_auto_stop bit) in CE-ATA transfers.

**List of Values that Cannot be Changed Before Command Issued:**

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
1274 ESP32-S3 TRM (Version 1.7)