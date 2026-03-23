

```markdown
| Signal No. | Input Signal   | Default value | Direct Input via IO MUX | Output Signal | Output enable signal when GPIO_FUNCn_OEN_SEL = 0 | Direct Output via IO MUX |
|------------|----------------|---------------|-------------------------|---------------|--------------------------------------------------|--------------------------|
| 0          | SPIQ_in        | 0             | yes                     | SPIQ_out      | SPIQ_oe                                          | yes                      |
| 1          | SPID_in        | 0             | yes                     | SPID_out      | SPID_oe                                          | yes                      |
| 2          | SPIHD_in       | 0             | yes                     | SPIHD_out     | SPIHD_oe                                         | yes                      |
| 3          | SPIWP_in       | 0             | yes                     | SPIWP_out     | SPIWP_oe                                         | yes                      |
| 4          | -              | -             | -                       | SPICLK_out_mux| SPICLK_oe                                        | yes                      |
| 5          | -              | -             | -                       | SPICS0_out    | SPICS0_oe                                        | yes                      |
| 6          | UORXD_in       | 0             | yes                     | UOTXD_out     | 1'd1                                             | yes                      |
| 7          | UOCTS_in       | 0             | no                      | UARTS_out     | 1'd1                                             | no                       |
| 8          | UODSR_in       | 0             | no                      | UODTR_out     | 1'd1                                             | no                       |
| 9          | U1RXD_in       | 0             | no                      | U1TXD_out     | 1'd1                                             | no                       |
| 10         | U1CTS_in       | 0             | no                      | U1RTS_out     | 1'd1                                             | no                       |
| 11         | U1DSR_in       | 0             | no                      | UIDTR_out     | 1'd1                                             | no                       |
| 12         | I2S_MCLK_in    | 0             | no                      | I2S_MCLK_out  | 1'd1                                             | no                       |
| 13         | I2SO_BCK_in    | 0             | no                      | I2SO_BCK_out  | 1'd1                                             | no                       |
| 14         | I2SO_WS_in     | 0             | no                      | I2SO_WS_out   | 1'd1                                             | no                       |
| 15         | I2SI_SD_in     | 0             | no                      | I2SO_SD_out   | 1'd1                                             | no                       |
| 16         | I2SI_BCK_in    | 0             | no                      | I2SI_BCK_out  | 1'd1                                             | no                       |
| 17         | I2SI_WS_in     | 0             | no                      | I2SI_WS_out   | 1'd1                                             | no                       |
| 18         | gpio_bt_priority| 0            | no                      | gpio_wlan_prio| 1'd1                                             | no                       |
| 19         | gpio_bt_active | 0             | no                      | gpio_wlan_active| 1'd1                                            | no                       |
| 20         | -              | -             | -                       | -             | 1'd1                                             | no                       |
| 21         | -              | -             | -                       | -             | 1'd1                                             | no                       |
| 22         | -              | -             | -                       | -             | 1'd1                                             | no                       |
| 23         | -              | -             | -                       | -             | 1'd1                                             | no                       |
| 24         | -              | -             | -                       | -             | 1'd1                                             | no                       |
```