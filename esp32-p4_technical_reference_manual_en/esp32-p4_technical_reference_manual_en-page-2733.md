

```markdown
load_new_cmd and data_expected and write data Block transfer

Tx Data Idle
    |
    |--- Stop data command -----------------> Tx Data stream
    |       |
    |       |--- load_new_cmd and data_expected and write data and stream transfer
    |
    |--- load_new_cmd and data_expected and write data and stream transfer ---> Rx CRC status
            |
            |--- Byte count remaining != 0 Data not busy ---> Tx Data block

Tx Data block
    |
    |--- Block done --------------------------> Rx Data block

Rx Data block
    |
    |--- Byte count Remaining != 0 Block done ---> Read wait

Read wait
    |
    |--- Byte count remaining == 0 or stop data command ---> Tx Data Idle

Figure 54.4-3. Data Transmit State Machine
```

```markdown
54.4.3.2 Data Receive

The module receives data two clock cycles after the end bit of a data read command, even if the command path detects a response error or a CRC error. If no response is received from the card and a response timeout occurs, the BIU does not receive a signal about the completion of the data transfer. If the command sent by the CIU is an illegal operation for the card, it would prevent the card from starting a read-data transfer, and the BIU will not receive a signal about the completion of the data transfer.

If no data is received by the data timeout, the data path signals a data timeout to the BIU, which marks an end to the data transfer. Based on the value of the SDHOST_TRANSFER_MODE bit in the SDHOST_CMD_REG register, the data receive state machine gets data from the card's data bus in a stream or block(s). The data receive state machine is shown in Figure 54.4-4.
```

```markdown
load_new_cmd and data_expected and read data and read block transfer

Tx Data Idle
    |
    |--- Stop data command -----------------> Rx Data stream
    |       |
    |       |--- load_new_cmd and data_expected and read data and stream transfer
    |
    |--- load_new_cmd and data_expected and read data and stream transfer ---> Read wait
            |
            |--- Byte count remaining == 0 or stop data command ---> Tx Data Idle

Rx Data stream
    |
    |--- Stop data command -----------------> Rx Data block

Rx Data block
    |
    |--- Byte count Remaining != 0 Block done ---> Read wait

Read wait
    |
    |--- Byte count remaining == 0 or stop data command ---> Tx Data Idle

Figure 54.4-4. Data Receive State Machine
```