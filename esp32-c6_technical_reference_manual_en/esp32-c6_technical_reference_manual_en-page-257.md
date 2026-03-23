

```markdown
| Signal No. | Input Signal         | Default value | Direct Input via IO MUX | Output Signal           | Output enable signal when GPIO_FUNCn_OEN_SEL = 0 | Direct Output via IO MUX |
|------------|----------------------|---------------|--------------------------|-------------------------|---------------------------------------------|----------------------------|
| 0          | ext_adc_start        | 0             | no                       | ledc_is_sig_outO        | 1'd1                                         | no                         |
| 1          | -                    | -             | -                        | ledc_is_sig_out1        | 1'd1                                         | no                         |
| 2          | -                    | -             | -                        | ledc_is_sig_out2        | 1'd1                                         | no                         |
| 3          | -                    | -             | -                        | ledc_is_sig_out3        | 1'd1                                         | no                         |
| 4          | -                    | -             | -                        | ledc_is_sig_out4        | 1'd1                                         | no                         |
| 5          | -                    | -             | -                        | ledc_is_sig_out5        | 1'd1                                         | no                         |
| 6          | UORXD_in             | 0              | yes                      | UOTXD_out               | 1'd1                                         | yes                        |
| 7          | UOCTS_in             | 0              | no                       | UORTS_out               | 1'd1                                         | no                         |
| 8          | UODSR_in             | 0              | no                       | UODTR_out               | 1'd1                                         | no                         |
| 9          | U1RXD_in             | 1              | no                       | U1TXD_out               | 1'd1                                         | no                         |
| 10         | U1CTS_in             | 0              | no                       | U1RTS_out               | 1'd1                                         | no                         |
| 11         | U1DSR_in             | 0              | no                       | U1DTR_out               | 1'd1                                         | no                         |
| 12         | I2S_MCLK_in          | 0              | no                       | I2S_MCLK_out            | 1'd1                                         | no                         |
| 13         | I2SO_BCK_in          | 0              | no                       | I2SO_BCK_out            | 1'd1                                         | no                         |
| 14         | I2SO_WS_in           | 0              | no                       | I2SO_WS_out             | 1'd1                                         | no                         |
| 15         | I2SI_SD_in           | 0              | no                       | I2SO_SD_out             | 1'd1                                         | no                         |
| 16         | I2SI_BCK_in          | 0              | no                       | I2SI_BCK_out            | 1'd1                                         | no                         |
| 17         | I2SI_WS_in           | 0              | no                       | I2SI_WS_out             | 1'd1                                         | no                         |
| 18         | -                    | -              | -                        | I2SO_SD1_out            | 1'd1                                         | no                         |
| 19         | usb_jtag_tdo_bridge  | 0              | no                       | usb_jtag_trst           | 1'd1                                         | no                         |
| 20         | -                    | -              | -                        | -                       | -                                            | -                          |
| 21         | -                    | -              | -                        | -                       | -                                            | -                          |
| 22         | -                    | -              | -                        | -                       | -                                            | -                          |
| 23         | -                    | -              | -                        | -                       | -                                            | -                          |
| 24         | -                    | -              | -                        | -                       | -                                            | -                          |
| 25         | -                    | -              | -                        | -                       | -                                            | -                          |
```