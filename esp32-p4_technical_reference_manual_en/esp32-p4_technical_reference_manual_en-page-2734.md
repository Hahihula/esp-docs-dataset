

```markdown
Chapter 54 SD/MMC Host Controller (SDHOST) GoBack


## 54.5 Software Restrictions for CIU Operations

* Only one card at a time can be selected to execute a command or data transfer. For example, when data are being transferred to or from a card, a new command must not be issued to another card. A new command, however, can be issued to the same card, allowing it to read the device status or stop the transfer.
* Only one data transfer command can be issued at a time.
* During an open-ended card write operation, if the card clock is stopped because RAM is empty, the software must first fill RAM with data, and start the card clock. Only then can it issue a stop/abort command to the card.
* During an SDIO/Combo card transfer, if the card function is suspended and the software wants to resume the suspended transfer, it must first reset and then release RAM by configuring the `SDHOST_FIFO_RESET` bit, and then issue the resume command as if it were a new data transfer command.
* When issuing card reset commands (CMDO, CMD15 or CMD52_reset) while a card data transfer is in progress, the software must set the `SDHOST_STOP_ABORT_CMD` bit in the `SDHOST_CMD_REG` register, so that the CIU can stop the data transfer after issuing the card reset command.
* When the controlling bit for end bit error is set in the `SDHOST_RINTSTS_REG` register, the CIU cannot control SDIO interrupts. In such a case, the software must ignore SDIO interrupts and issue a stop/abort command to the card, so that the card stops transmitting data.
* If the card clock is stopped because RAM is full during a card read, the software must read at least two RAM addresses to restart the card clock.
* Only one CE-ATA device at a time can be selected for a command or data transfer. For example, when data are transferred from a CE-ATA device, a new command must not be sent to another CE-ATA device.
* If the CE-ATA device interrupts are enabled (`nIEN=0`), a new `SDHOST_RW_BLK` command must not be sent to the same device if the execution of a `SDHOST_RW_BLK` command is already in progress. Only the Command Completion Signal Disable (CCSD) command can be sent while waiting for the Command Completion Signal (CCS).
* If, however, the CE-ATA device interrupts are disabled (`nIEN=1`), a new command can be issued to the same device, allowing it to read status information.
* Open-ended transfers are not supported for CE-ATA devices.
* The `sdhost_send_auto_stop` signal is not supported (software must not set the `SDHOST_SEND_AUTO_STOP` bit) for CE-ATA transfers.

After configuring the command start bit to 1, the values of the following registers cannot be changed before a command has been issued:

* CMD - command
* CMDARG - command argument
* BYTCNT - byte count
* BLKSIZ - block size
* CLKDIV - clock divider
```