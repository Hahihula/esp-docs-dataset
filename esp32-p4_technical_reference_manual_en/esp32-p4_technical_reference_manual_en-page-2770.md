

```markdown
Register 54.35. SDHOST_STATUS_REG (0x0048)

Continued from the previous page...

SDHOST_COMMAND_FSM_STATES Represents the command FSM states.

0x0: Idle
0x1: Send init sequence
0x2: Send cmd start bit
0x3: Send cmd tx bit
0x4: Send cmd index + arg
0x5: Send cmd crc7
0x6: Send cmd end bit
0x7: Receive resp start bit
0x8: Receive resp IRQ response
0x9: Receive resp tx bit
0xA: Receive resp cmd idx
0xB: Receive resp data
0xC: Receive resp crc7
0xD: Receive resp end bit
0xE: Cmd path wait NOC
0xF: Wait, cmd-to-response turnaround (RO)

SDHOST_DATA_3_STATUS Represents the value of the sdhost_card_data[3] signal, which indicates whether card is present.

0: Card not present
1: Card present (RO)

SDHOST_DATA_BUSY Represents inverted value of the sdhost_card_data[0] signal, which indicates card data is busy.

0: Card data not busy
1: Card data busy (RO)

SDHOST_DATA_STATE_MC_BUSY Represents whether the data transmit or receive state-machine is busy.

0: Not busy
1: Busy (RO)

SDHOST_RESPONSE_INDEX Represents index of previous response, including any auto-stop sent by core. (RO)

SDHOST_FIFO_COUNT Represents FIFO count, number of filled locations in FIFO. (RO)
```