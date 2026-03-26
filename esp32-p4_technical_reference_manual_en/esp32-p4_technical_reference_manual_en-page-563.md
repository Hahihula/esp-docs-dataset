

```markdown
| Signal No. | Input Signal           | Default value | Direct Input via LP IO MUX | Output Signal         | Output enable signal when LP_GPIO_FUNCn_OE_SEL = 0 | Direct Output via LP IO MUX |
|------------|------------------------|---------------|----------------------------|-----------------------|--------------------------------------------------|------------------------------|
| 0          | lp_i2c_scl_pad_in      | 1             | no                         | lp_i2c_scl_pad_out    | lp_i2c_scl_pad_oE                                | no                           |
| 1          | lp_i2c_sda_pad_in      | 1             | no                         | lp_i2c_sda_pad_out    | lp_i2c_sda_pad_oE                                | no                           |
| 2          | lp_uart_rxd_pad_in     | 0             | yes                        | lp_uart_txd_pad_out   | '1'd1                                             | yes                          |
| 3          | lp_uart_ctsn_pad_in    | 1             | no                         | lp_uart_rtsh_pad_out  | '1'd1                                             | no                           |
| 4          | lp_uart_dsmn_pad_in    | 1             | no                         | lp_uart_dtrn_pad_out  | '1'd1                                             | no                           |
| 5          | lp_spi_ck_pad_in       | 0             | no                         | lp_spi_ck_pad_out     | lp_spi_ck_pad_oE                                 | no                           |
| 6          | lp_spi_cs_pad_in       | 0             | no                         | lp_spi_cs_pad_out     | lp_spi_cs_pad_oE                                 | no                           |
| 7          | lp_spi_d_pad_in        | 0             | no                         | lp_spi_d_pad_out      | lp_spi_d_pad_oE                                  | no                           |
| 8          | lp_spi_q_pad_in        | 0             | no                         | lp_spi_q_pad_out      | lp_spi_q_pad_oE                                  | no                           |
| 9          | lp_i2s_i_bck_pad_in    | 0             | no                         | lp_i2s_i_bck_pad_out  | '1'd1                                             | no                           |
| 10         | lp_i2s_i_sd_pad_in     | 0             | no                         | lp_i2s_o_sd_pad_out   | '1'd1                                             | no                           |
| 11         | lp_i2s_i_ws_pad_in     | 0             | no                         | lp_i2s_i_ws_pad_out   | '1'd1                                             | no                           |
| 12         | lp_i2s_o_bck_pad_in    | 0             | no                         | lp_i2s_o_bck_pad_out  | '1'd1                                             | no                           |
| 13         | lp_i2s_o_ws_pad_in     | 0             | no                         | lp_i2s_o_ws_pad_out   | '1'd1                                             | no                           |
| 14         | -                      | -             | -                          | -                     | -                                                | -                            |
| 15         | -                      | -             | -                          | -                     | -                                                | -                            |
| 16         | -                      | -             | -                          | -                     | -                                                | -                            |
| 17         | -                      | -             | -                          | -                     | -                                                | -                            |
| 18         | -                      | -             | -                          | -                     | -                                                | -                            |
| 19         | -                      | -             | -                          | -                     | -                                                | -                            |
| 20         | -                      | -             | -                          | -                     | -                                                | -                            |
| 21         | -                      | -             | -                          | -                     | -                                                | -                            |
| 22         | -                      | -             | -                          | -                     | -                                                | -                            |
| 23         | -                      | -             | -                          | -                     | -                                                | -                            |
```