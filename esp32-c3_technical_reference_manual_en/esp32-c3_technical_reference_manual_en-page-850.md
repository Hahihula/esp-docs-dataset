

```markdown
| Register                  | Bit/Field Configuration Update                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------|
|                            | RX Channels                                                                                     |
| RMT_CHmCONFO_REG          | RMT_CARRIER_OUT_LV_CHm<br>RMT_CARRIER_EN_CHm<br>RMT_IDLE_THRES_CHm<br>RMT_DIV_CNT_CHm |
| RMT_CHmCONF1_REG           | RMT_RX_FILTER_THRES_CHm<br>RMT_RX_EN_CHm<br>RMT_CARRIER_HIGH_THRES_CHm<br>RMT_CARRIER_LOW_THRES_CHm |
| RMT_CHm_RX_CARRIER_RM_REG  |                                                                                                 |
| RMT_CHm_RX_LIM_REG         | RMT_RX_LIM_CHm                                                                                  |
| RMT_REF_CNT_RST_REG        | RMT_REF_CNT_RST_CHm                                                                             |

## 33.3.7 Interrupts

*   `RMT_CHn/m_ERR_INT`: triggered when channel `n/m` does not read or write data correctly. For example, if the transmitter still tries to read data from RAM when the RAM is empty, or the receiver still tries to write data into RAM when the RAM is full, this interrupt will be triggered.
*   `RMT_CHn_TX_THR_EVENT_INT`: triggered when the amount of data the transmitter has sent matches the value of `RMT_CHn_TX_LIM_REG`.
*   `RMT_CHm_RX_THR_EVENT_INT`: triggered each time when the amount of data received by the receiver reaches the value set in `RMT_CHm_RX_LIM_REG`.
*   `RMT_CHn_TX_END_INT`: Triggered when the transmitter has finished transmitting signals.
*   `RMT_CHm_RX_END_INT`: Triggered when the receiver has finished receiving signals.
*   `RMT_CHn_TX_LOOP_INT`: Triggered when the loop counting reaches the value set by `RMT_TX_LOOP_NUM_ChN`.
```