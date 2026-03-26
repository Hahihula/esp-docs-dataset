

```markdown
Register 54.29. SDHOST_IDSTS_REG (0x008C)

Continued from the previous page...

SDHOST_IDISTS_FBE_CODE Represents the type of error that caused a Bus Error, valid only when SDHOST_IDISTS_REG[2] is set.
    0x1: Host Abort received during transmission
    0x2: Host Abort received during reception
Others: Reserved
(RO)

SDHOST_IDISTS FSM Represents DMA FSM present state.
    0x0: DMA_IDLE (idle state)
    0x1: DMA_SUSPEND (suspend state)
    0x2: DESC_RD (descriptor reading state)
    0x3: DESC_CHK (descriptor checking state)
    0x4: DMA_RD_REQ_WAIT (read-data request waiting state)
    0x5: DMA_WR_REQ_WAIT (write-data request waiting state)
    0x6: DMA_RD (data-read state)
    0x7: DMA_WR (data-write state)
    0x8: DESC_CLOSE (descriptor close state)
(RO)

Register 54.30. SDHOST_IDINTEN_REG (0x0090)
```

```markdown
| Bit | Name                     | Description                                                                 |
|-----|--------------------------|-----------------------------------------------------------------------------|
| 31  |                          | Reset                                                                       |
|     |                          | (reserved)                                                                  |
| 30  | SDHOST_IDINTEN_AI        | Write 1 to enable interrupt of Abnormal Interrupt Summary. (R/W)            |
| 29  | SDHOST_IDINTEN_NI        | Write 1 to enable interrupt of Normal Interrupt Summary. (R/W)              |
| 28  | SDHOST_IDINTEN_CES       | Write 1 to enable interrupt of Card Error summary. (R/W)                    |
| 27  | SDHOST_IDINTEN_DU        | Write 1 to enable interrupt of Descriptor Unavailable. (R/W)                |
| 26  | SDHOST_IDINTEN_FBE       | Write 1 to enable interrupt of Fatal Bus Error. (R/W)                       |
| 25  | SDHOST_IDINTEN_RI        | Write 1 to enable interrupt of Receive. (R/W)                               |
| 24  | SDHOST_IDINTEN_TI        | Write 1 to enable interrupt of Transmit.(R/W)                               |
```