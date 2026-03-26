

```markdown
Register 54.10. SDHOST_CMD_REG (0x002C)

Continued from the previous page...

SDHOST_WAIT_PRVDATA_COMPLETE Configures whether to send command at once.
    0: Send command at once, even if previous data transfer has not completed
    1: Wait for previous data transfer to complete before sending Command
        (R/W)

SDHOST_STOP_ABORT_CMD Configures whether the stop/abort command stops data transfer.
    0: Neither stop nor abort command can stop the current data transfer. If abort is sent to the card device currently selected, or the card device is not in data-transfer mode, then bit should be set to 0
    1: Stop or abort command intended to stop current data transfer in progress
        (R/W)

SDHOST_SEND_INITIALIZATION Configures whether to send initialization sequence (80 clocks of 1) before sending this command. After powered on, 80 clocks must be sent to card for initialization before sending any commands to card. Bit should be set while sending the first command to card so that the controller will initialize clocks before sending command to card.
    0: Do not send initialization sequence before sending this command
    1: Send initialization sequence before sending this command
        (R/W)

SDHOST_CARD_NUMBER Configures card number in use, the physical slot number of the card being accessed. In SD-only mode, up to two cards are supported. (R/W)

SDHOST_UPDATE_CLOCK_REGISTERS_ONLY Configures whether to only update clock register value into card clock domain.
    Following register values are transferred into card clock domain: SDHOST_CLKDIV_REG, SD-HOST_CLRSRC_REG, and SDHOST_CLKENA_REG.
    When this bit is set, there will be no Command Done interrupts because no command is sent to SD_MMC_CEATA cards.
        0: Normal command sequence
        1: Do not send commands, just update clock register value into card clock domain
            (R/W)

SDHOST_READ_CEATA_DEVICE Configures whether to read access CE-ATA device.
    This bit is used to disable read data timeout indication while performing CE-ATA read transfers.
    0: Host is not performing read access (RW_REG or RW_BLK)towards CE-ATA device
    1: Host is performing read access (RW_REG or RW_BLK) towards CE-ATA device
        (R/W)

Continued on the next page...
```