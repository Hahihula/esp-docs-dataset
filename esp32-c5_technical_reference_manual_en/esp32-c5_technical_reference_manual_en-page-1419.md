

```markdown
Register 38.22. TWAIFD_TX_STATUS_REG (0x0070)

| 31 | 28 | 27 | 24 | 23 | 20 | 19 | 16 | 15 | 12 | 11 | 8 | 7 | 4 | 3 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|
| OxO | OxO |    |    |    | OxO | OxO |    |    | Ox8 | Ox8 |   |   |   |   | Reset |

TWAIFD_TXTBO_STATE Represents the status of TX buffer 1.
0: TXT_NOT_EXIST - TX buffer does not exist in the core (applies when CAN FDis synthesized with fewer than 8 TX buffers).
1: TXT_RDY - TX buffer is in "ready" state, waiting for CAN FDto start transmission
2: TXT_TRAN - TX buffer is in "TX in progress" state; CAN FDis transmitting a frame
3: TXT_ABTP - TX buffer is in "abort in progress" state
4: TXT_TOK - TX buffer is in "TX OK" state
6: TXT_ERR - TX buffer is in "failed" state
7: TXT_ABT - TX buffer is in "aborted" state
8: TXT_ETY - TX buffer is in "empty" state (RO)

TWAIFD_TX2S Represents the status of TX buffer 2. Refer to TWAIFD_TXTBO_STATE for field values. (RO)
TWAIFD_TX3S Represents the status of TX buffer 3. Refer to TWAIFD_TXTBO_STATE for field values. (RO)
TWAIFD_TX4S Represents the status of TX buffer 4. Refer to TWAIFD_TXTBO_STATE for field values. (RO)
TWAIFD_TX5S Represents the status of TX buffer 5. Refer to TWAIFD_TXTBO_STATE for field values. (RO)
TWAIFD_TX6S Represents the status of TX buffer 6. Refer to TWAIFD_TXTBO_STATE for field values. (RO)
TWAIFD_TX7S Represents the status of TX buffer 7. Refer to TWAIFD_TXTBO_STATE for field values. (RO)
TWAIFD_TX8S Represents the status of TX buffer 8. Refer to TWAIFD_TXTBO_STATE for field values. (RO)
```