

```markdown
Register 52.7. DMAOPERATION_MODE_REG (0x1018)

Continued from the previous page...

START_STOP_TRANSMISSION_COMMAND Configures whether to start or stop the transmission.
    0: Stop
    1: Start
        (R/W)

FWD_ERR_FRAME Configures whether RX FIFO forward frames with error status (CRC error, collision error, giant frame, watchdog timeout, or overflow)
    0: Drop
    1: Forward
        (R/W)

FWD_UNDER_GF Configures whether the RX FIFO forward undersized (frames with no Error and length less than 64 bytes) good frames including PAD and CRC.
    0: Drop
    1: Forward
        (R/W)

DROP_GFRM Configures whether to the ETH_MAC drops the received giant frames in the RX FIFO.
    0: Not drop
    1: Drop
        (R/W)

RX_THRESH_CTRL Configures the threshold of the RX FIFO.
    0: 64
    1: 32
    2: 96
    3: 128
Transfer (request) to DMA starts when the frame size within the RX FIFO is larger than the threshold. (R/W)

OPT_SECOND_FRAME Configures whether the DMA processes the second frame of the Transmit data even before the status for the first frame is obtained.
    0: Not process
    1: Process
        (R/W)

START_STOP_RX Configures whether to start or stop RX DMA reception.
    0: Stop reception after the transfer of the current frame
    1: Start reception
        (R/W)
```