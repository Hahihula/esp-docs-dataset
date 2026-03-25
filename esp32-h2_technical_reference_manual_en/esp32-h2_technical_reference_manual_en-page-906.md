

```markdown
- Configure I2S_RX_STOP_MODE to control data reception suspension:
  * 0: The RX unit only suspends data reception when I2S_RX_START is cleared.
  * 1: The RX unit suspends data reception when the number of received bytes is greater than the value configured in I2S_RX_EOF_NUM_REG. When I2S_RX_START is not cleared, data reception can be restarted by setting I2S_RX_RESET to 1.
  * 2: The RX unit suspends data reception when I2S_RX_START is cleared or GDMA RX FIFO is full. When I2S_RX_START is not cleared and the GDMA RX FIFO is no longer full, data reception can be restarted by setting I2S_RX_RESET to 1.

- The RX unit stops receiving data when I2S_RX_START is cleared.
```

## 31.9 Transmitting Data

**Note:**
Updating the configuration described in this and subsequent sections requires to set `I2S_TX_UPDATE` accordingly to synchronize registers from APB clock domain to TX clock domain. For more detailed configurations, see Section 31.13.1.

In TX mode, I2S first reads data through GDMA and transmits these data out via output signals according to the configured data mode and channel mode.

### 31.9.1 Data Format Control

Data format is controlled in the following phases:

* Phase I: Read data from memory and write it to TX FIFO;
* Phase II: Read the TX data from TX FIFO and convert the data according to the output data mode;
* Phase III: Clock out the TX data serially.

#### 31.9.1.1 Bit Width Control of Channel Valid Data

The bit width of the valid data in each channel is determined by `I2S_TX_BITS_MOD` and `I2S_TX_24_FILL_EN`. For details, see the table below.

Table 31.9-1. Bit Width of Channel Valid Data

| Channel Valid Data Width | I2S_TX_BITS_MOD | I2S_TX_24_FILL_EN |
|--------------------------|------------------|-------------------|
| 32                       | 31               | x*                |
|                          | 23               | 1                 |
| 24                       | 23               | 0                 |
| 16                       | 15               | x                 |
| 8                        | 7                | x                 |

\* "x" represents that this value is ignored (applies to all tables in this chapter).
```