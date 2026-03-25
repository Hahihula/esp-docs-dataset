

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| ID Register                                |                                                                             |           |        |
| TWAIFD_DEVICE_ID_VERSION_REG               | Device ID status register                                                   | 0x0000    | RO     |
| Configuration Register                     |                                                                             |           |        |
| TWAIFD_MODE_SETTINGS_REG                   | Mode setting register                                                       | 0x0004    | varies |
| TWAIFD_COMMAND_REG                         | Command register                                                            | 0x000C    | WO     |
| TWAIFD_BTR_REG                             | Bit time register                                                           | 0x0024    | R/W    |
| TWAIFD_BTR_FD_REG                          | Segment bit time of FD register                                             | 0x0028    | R/W    |
| TWAIFD_TRV_DELAY_SSP_CFG_REG               | Transmission delay & secondary sample point configuration register        | 0x0080    | varies |
| TWAIFD_TIMER_CLK_EN_REG                    | Timer clock force enable register                                           | 0x0FD4    | R/W    |
| TWAIFD_TIMER_CFG_REG                       | Timer configuration register                                                 | 0x0FE8    | varies |
| TWAIFD_TIMER_LD_VAL_L_REG                  | Timer pre-load value register                                                | 0x0FEC    | R/W    |
| TWAIFD_TIMER_CT_VAL_L_REG                  | Timer count-to value register                                                | 0x0FF4    | R/W    |
| Status Register                            |                                                                             |           |        |
| TWAIFD_STATUS_REG                          | Status register                                                             | 0x0008    | RO     |
| TWAIFD_RX_MEM_INFO_REG                     | RX memory information register                                               | 0x0060    | RO     |
| TWAIFD_RX_POINTERS_REG                     | RX memory pointer information register                                       | 0x0064    | RO     |
| TWAIFD_RX_STATUS_RX_SETTINGS_REG           | RX status & setting register                                                 | 0x0068    | varies |
| TWAIFD_TX_STATUS_REG                       | TX buffer status register                                                   | 0x0070    | RO     |
| TWAIFD_ERR_CAPT_RETR_CTR_ALC_TS_INFO_REG   | Error capture & retransmission counter & arbitration lost & timestamp integration information register | 0x007C    | RO     |
| TWAIFD_TIMESTAMP_LOW_REG                   | Lower part of the time base register                                         | 0x0094    | RO     |
| TWAIFD_TIMESTAMP_HIGH_REG                  | Higher part of the time base register                                        | 0x0098    | RO     |
| Interrupt Register                         |                                                                             |           |        |
| TWAIFD_INT_STAT_REG                        | Masked interrupt status register                                             | 0x0010    | R/W1C  |
| TWAIFD_INT_ENA_SET_REG                     | Interrupt enable register                                                    | 0x0014    | R/W1S  |
| TWAIFD_INT_ENA_CLR_REG                     | Interrupt clear register                                                     | 0x0018    | WO     |
| TWAIFD_INT_MASK_SET_REG                    | Masked interrupt status register                                             | 0x001C    | R/W1S  |
| TWAIFD_INT_MASK_CLR_REG                    | Masked interrupt clear register                                              | 0x0020    | WO     |
| TWAIFD_TIMER_INT_RAW_REG                   | Timer raw interrupt status register                                          | 0x0FD8    | R/SS/WTC|
| TWAIFD_TIMER_INT_ST_REG                    | Timer masked interrupt status register                                       | 0x0FDC    | RO     |
| TWAIFD_TIMER_INT_ENA_REG                   | Timer interrupt enable register                                              | 0x0FE0    | R/W    |
| TWAIFD_TIMER_INT_CLR_REG                   | Timer interrupt clear register                                               | 0x0FE4    | WT     |
| Error Confinement Register                 |                                                                             |           |        |
| TWAIFD_EWL_ERP_FAULT_STATE_REG             | Error threshold and status register                                          | 0x002C    | varies |
```