

```markdown
| Register                     | Bit/Field Configuration Update                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------|
| TX Channel                   |                                                                                                |
|                              | RMT_CARRIER_OUT_LV_CHn                                                                          |
|                              | RMT_CARRIER_EN_CHn                                                                              |
|                              | RMT_CARRIER_EFF_EN_CHn                                                                          |
|                              | RMT_DIV_CNT_CHn                                                                                 |
| RMT_CHnCONFO_REG             | RMT_TX_STOP_CHn                                                                                  |
|                              | RMT_IDLE_OUT_EN_CHn                                                                              |
|                              | RMT_IDLE_OUT_LV_CHn                                                                              |
|                              | RMT_TX_CONTI_MODE_CHn                                                                            |
| RMT_CHnCARRIER_DUTY_REG      | RMT_CARRIER_HIGH_CHn                                                                             |
|                              | RMT_CARRIER_LOW_CHn                                                                              |
| RMT_CHnTX_LIM_REG            | RMT_TX_LOOP_CNT_EN_CHn                                                                           |
|                              | RMT_TX_LOOP_NUM_CHn                                                                              |
|                              | RMT_TX_LIM_CHn                                                                                    |
| RMT_TX_SIM_REG               | RMT_TX_SIM_EN                                                                                   |
| RX Channel                   |                                                                                                |
|                              | RMT_CARRIER_OUT_LV_CHm                                                                           |
| RMT_CHmCONFO_REG             | RMT_CARRIER_EN_CHm                                                                               |
|                              | RMT_IDLE_THRES_CHm                                                                               |
|                              | RMT_DIV_CNT_CHm                                                                                  |
| RMT_CHmCONF1_REG             | RMT_RX_FILTER_THRES_CHm                                                                          |
|                              | RMT_RX_EN_CHm                                                                                    |
| RMT_CHmRX_CARRIER_RM_REG     | RMT_CARRIER_HIGH_THRES_CHm                                                                       |
|                              | RMT_CARRIER_LOW_THRES_CHm                                                                        |
| RMT_CHmRX_LIM_REG            | RMT_RX_LIM_CHm                                                                                   |
| RMT_REF_CNT_RST_REG          | RMT_REF_CNT_RST_CHm                                                                              |

## 57.4 Interrupts

ESP32-P4's RMT can generate the RMT_INTR interrupt signal that will be sent to the **Interrupt Matrix**.

The following interrupt sources can generate the RMT_INTR interrupt signal:

*   `RMT_CHn_ERR_INT`: Triggered when channel *n* does not read or write data correctly. For example, the transmitter still tries to read data from RAM when the RAM is empty.
*   `RMT_CHm_ERR_INT`: Triggered when channel *m* does not read or write data correctly. For example, the receiver still tries to write data into RAM when the RAM is full.
*   `RMT_CHn_TX_THR_EVENT_INT`: Triggered when the amount of data the transmitter has sent matches the value of `RMT_CHn_TX_LIM_REG`.
*   `RMT_CHm_RX_THR_EVENT_INT`: Triggered each time when the amount of data received by the receiver reaches the value set in `RMT_CHm_RX_LIM_REG`.
*   `RMT_CHn_TX_END_INT`: Triggered when the transmitter has finished transmitting signals.
```