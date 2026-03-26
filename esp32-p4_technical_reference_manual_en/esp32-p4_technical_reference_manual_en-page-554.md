

```markdown
| Signal No.| Input Signal          | Default Value | Direct Input via HP IO MUX | Output Signal         | Output Enable Signal when GPIO_FUNCn_OE_SEL = 0 | Direct Output via HP IO MUX |
|-----------|-----------------------|---------------|----------------------------|------------------------|---------------------------------------------|------------------------------|
| 55        | spi2_d_pad_in         | 0             | yes                        | spi2_d_pad_out         | spi2_d_pad_oe                               | yes                          |
| 56        | spi2_hold_pad_in      | 0             | yes                        | spi2_hold_pad_out      | spi2_hold_pad_oe                            | yes                          |
| 57        | spi2_wp_pad_in        | 0             | yes                        | spi2_wp_pad_out        | spi2_wp_pad_oe                              | yes                          |
| 58        | spi2_io4_pad_in       | 0             | yes                        | spi2_io4_pad_out       | spi2_io4_pad_oe                             | yes                          |
| 59        | spi2_io5_pad_in       | 0             | yes                        | spi2_io5_pad_out       | spi2_io5_pad_oe                             | yes                          |
| 60        | spi2_io6_pad_in       | 0             | yes                        | spi2_io6_pad_out       | spi2_io6_pad_oe                             | yes                          |
| 61        | spi2_io7_pad_in       | 0             | yes                        | spi2_io7_pad_out       | spi2_io7_pad_oe                             | yes                          |
| 62        | spi2_cs_pad_in        | 0             | yes                        | spi2_cs_pad_out        | spi2_cs_pad_oe                              | yes                          |
| 63        | pcnt_rst_pad_in0      | 0             | no                         | spi2_cs1_pad_out       | spi2_cs1_pad_oe                             | no                           |
| 64        | pcnt_rst_pad_in1      | 0             | no                         | spi2_cs2_pad_out       | spi2_cs2_pad_oe                             | no                           |
| 65        | pcnt_rst_pad_in2      | 0             | no                         | spi2_cs3_pad_out       | spi2_cs3_pad_oe                             | no                           |
| 66        | pcnt_rst_pad_in3      | 0             | no                         | spi2_cs4_pad_out       | spi2_cs4_pad_oe                             | no                           |
| 67        | -                     | -             | -                          | spi2_cs5_pad_out       | spi2_cs5_pad_oe                             | no                           |
| 68        | i2c0_scl_pad_in       | 1             | no                         | i2c0_scl_pad_out       | i2c0_scl_oe_pad_out                         | no                           |
| 69        | i2c0_sda_pad_in       | 1             | no                         | i2c0_sda_pad_out       | i2c0_sda_oe_pad_out                         | no                           |
| 70        | i2c1_scl_pad_in       | 1             | no                         | i2c1_scl_pad_out       | i2c1_scl_oe_pad_out                         | no                           |
| 71        | i2c1_sda_pad_in       | 1             | no                         | i2c1_sda_pad_out       | i2c1_sda_oe_pad_out                         | no                           |
| 72        | -                     | -             | -                          | gpio_sd0_out           | 'd1                                        | no                           |
| 73        | -                     | -             | -                          | gpio_sd1_out           | 'd1                                        | no                           |
| 74        | uart0_slp_clk_pad_in  | 0             | no                         | gpio_sd2_out           | 'd1                                        | no                           |
| 75        | uart1_slp_clk_pad_in  | 0             | no                         | gpio_sd3_out           | 'd1                                        | no                           |
| 76        | uart2_slp_clk_pad_in  | 0             | no                         | gpio_sd4_out           | 'd1                                        | no                           |
| 77        | uart3_slp_clk_pad_in  | 0             | no                         | gpio_sd5_out           | 'd1                                        | no                           |
| 78        | uart4_slp_clk_pad_in  | 0             | no                         | gpio_sd6_out           | 'd1                                        | no                           |
| 79        | -                     | -             | -                          | gpio_sd7_out           | 'd1                                        | no                           |
| 80        | twai0_rx_pad_in       | 1             | no                         | twai0_tx_pad_out       | 'd1                                        | no                           |
| 81        | -                     | -             | -                          | twai0_bus_off_on_pad_out | 'd1                                       | no                           |
| 82        | -                     | -             | -                          | twai0_clkout_pad_out   | 'd1                                       | no                           |
```