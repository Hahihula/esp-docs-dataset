**Table: Signal Mapping**

| **Signal No.** | Input Signals | Default Value If Unassigned* | Same Input Signal from IO_MUX Core | Output Signals | Output Enable of Output Signals |
|----------------|---------------|------------------------------|-------------------------------------|----------------|---------------------------------|
| 184            | —             | —                            | I2S1O_DATA_out18                    | 1'd1           |
| 185            | —             | —                            | I2S1O_DATA_out19                    | 1'd1           |
| 186            | —             | —                            | I2S1O_DATA_out20                    | 1'd1           |
| 187            | —             | —                            | I2S1O_DATA_out21                    | 1'd1           |
| 188            | —             | —                            | I2S1O_DATA_out22                    | 1'd1           |
| 189            | —             | —                            | I2S1O_DATA_out23                    | 1'd1           |
| 190            | I2SOI_H_SYNC  | O                             | no                                   | pwm3_out1h     | 1'd1                           |
| 191            | I2SOI_V_SYNC  | O                             | no                                   | pwm3_out1l     | 1'd1                           |
| 192            | I2SOI_H_ENABLE| O                             | no                                   | pwm3_out2h     | 1'd1                           |
| 193            | I2S1I_H_SYNC  | O                             | no                                   | pwm3_out2l     | 1'd1                           |
| 194            | I2S1I_V_SYNC  | O                             | no                                   | pwm3_out3h     | 1'd1                           |
| 195            | I2S1I_H_ENABLE| O                             | no                                   | pwm3_out3l     | 1'd1                           |
| 196            | —             | —                            | pwm3_out4h                          | 1'd1           |
| 197            | —             | —                            | pwm3_out4l                          | 1'd1           |
| 198            | U2RXD_in      | O                             | yes                                  | U2TXD_out      | 1'd1                           |
| 199            | U2CTS_in      | O                             | yes                                  | U2RTS_out      | 1'd1                           |
| 200            | emac_mdc_i    | O                             | no                                   | emac_mdc_o     | emac_mdc_oe                  |
| 201            | emac_mdi_i    | O                             | no                                   | emac_mdo_o     | emac_mdo_o_e                 |
| 202            | emac_crs_i    | O                             | no                                   | emac_crs_o     | emac_crs_oe                  |
| 203            | emac_col_i    | O                             | no                                   | emac_col_o     | emac_col_oe                  |
| 204            | pcmfsync_in   | O                             | no                                   | bt_audio0_irq   | 1'd1                           |
| 205            | pcmclk_in     | O                             | no                                   | bt_audio1_irq   | 1'd1                           |
| 206            | pcmdin        | O                             | no                                   | bt_audio2_irq   | 1'd1                           |
| 207            | —             | —                            | ble_audio0_irq                        | 1'd1           |
| 208            | —             | —                            | ble_audio1_irq                        | 1'd1           |
| 209            | —             | —                            | ble_audio2_irq                        | 1'd1           |

*Note: The table includes a note about "Unassigned" signals, but no specific details are provided in the image.