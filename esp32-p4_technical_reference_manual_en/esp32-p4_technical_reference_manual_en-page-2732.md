

```markdown
## 54.4.2 Command Path

The command path performs the following functions:

* Configures clock parameters
* Configures card command parameters
* Sends commands to card bus (sdhost_ccmd_out line)
* Receives responses from card bus (sdhost_ccmd_in line)
* Sends responses to BIU
* Drives the P-bit on the command line

The command path state machine is shown in Figure 54.4-2.

![Figure 54.4-2. Command Path State Machine](image_path_if_available)

## 54.4.3 Data Path

The data path block pops RAM data and transmits them on sdhost_cdata_out during a write-data transfer, or it receives data on sdhost_cdata_in and pushes them into RAM during a read-data transfer. The data path loads new data parameters, i.e., expected data, read/write data transfer, stream/block transfer, block size, byte count, card type, timeout registers, etc., whenever a data transfer command is not in progress.

If the SDHOST_DATA_EXPECTED bit is set in the SDHOST_CMD_REG register, the new command is a data transfer command and the data path starts one of the following operations:

* Transmitting data if the SDHOST_READ_WRITE bit is 1
* Receiving data if the SDHOST_READ_WRITE bit is 0

### 54.4.3.1 Data Transmit

The module starts data transmission two clock cycles after a response for the data write command is received. This occurs even if the command path detects a response error or a cyclic redundancy check (CRC) error in a response. If no response is received from the card until the response timeout, no data will be transmitted. Depending on the value of the SDHOST_TRANSFER_MODE bit in the SDHOST_CMD_REG register, the data transmit state machine adds data to the card’s data bus in a stream or in block(s). The data transmit state machine is shown in Figure 54.4-3.
```