

```markdown
Register 52.6. DMASTATUS_REG (0x1014)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 23 | 22 | 20 | 19 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0x0| 0x0|    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset |
```

EMAC_LPI_INT The raw interrupt status of EMAC_LPI_INT. (RO)

TS_TRI_INT The raw interrupt status of TS_TRI_INT. (RO)

EMAC_PMT_INT The raw interrupt status of EMAC_PMT_INT. (RO)

ERROR_BITS Represents the type of error that caused a Bus Error, for example, error response on the AHB interface.

0: Error during RX DMA Write Data Transfer
1: Error during TX DMA Read Data Transfer
2: Error during RX DMA Descriptor Write Access
3: Error during TX DMA Descriptor Write Access
4: Error during RX DMA Descriptor Read Access
5: Error during TX DMA Descriptor Read Access

Valid only when Bit 13 (FBI) is 1. This field does not generate an interrupt. (RO)

TRANS_PROC_STATE Represents the Transmit DMA FSM state.

0: Stopped; Reset or Stop Transmit Command issued
1: Running; Fetching Transmit Transfer Descriptor
2: Running; Waiting for status
3: Running; Reading Data from Host memory buffer and queuing it to transmit buffer (TX FIFO)
4: TIME_STAMP write state
5: Reserved for future use
6: Suspended; Transmit Descriptor Unavailable or Transmit Buffer Underflow
7: Running; Closing Transmit Descriptor

This field does not generate an interrupt. (RO)

Continued on the next page...
```