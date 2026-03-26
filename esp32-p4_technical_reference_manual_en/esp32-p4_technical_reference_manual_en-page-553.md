

```markdown
| Signal No.| Input Signal                     | Default Value | Direct Input via HP IO MUX | Output Signal                  | Output Enable Signal when GPIO_FUNCn_OE_SEL = 0 | Direct Output via HP IO MUX |
|-----------|-----------------------------------|---------------|-----------------------------|---------------------------------|----------------------------------------------|------------------------------|
| 27        | i2s0_o_ws_pad_in                 | 0             | no                          | i2s0_o_ws_pad_out               | '1'd1                                       | no                           |
| 28        | i2s0_i_sd_pad_in                 | 0             | no                          | i2s0_o_sd_pad_out               | '1'd1                                       | no                           |
| 29        | i2s0_i_bck_pad_in                | 0             | no                          | i2s0_i_bck_pad_out              | '1'd1                                       | no                           |
| 30        | i2s0_i_ws_pad_in                 | 0             | no                          | i2s0_i_ws_pad_out               | '1'd1                                       | no                           |
| 31        | i2s1_o_bck_pad_in                | 0             | no                          | i2s1_o_bck_pad_out              | '1'd1                                       | no                           |
| 32        | i2s1_mclk_pad_in                 | 0             | no                          | i2s1_mclk_pad_out               | '1'd1                                       | no                           |
| 33        | i2s1_o_ws_pad_in                 | 0             | no                          | i2s1_o_ws_pad_out               | '1'd1                                       | no                           |
| 34        | i2s1_i_sd_pad_in                 | 0             | no                          | i2s1_o_sd_pad_out               | '1'd1                                       | no                           |
| 35        | i2s1_i_bck_pad_in                | 0             | no                          | i2s1_i_bck_pad_out              | '1'd1                                       | no                           |
| 36        | i2s1_i_ws_pad_in                 | 0             | no                          | i2s1_i_ws_pad_out               | '1'd1                                       | no                           |
| 37        | i2s2_o_bck_pad_in                | 0             | no                          | i2s2_o_bck_pad_out              | '1'd1                                       | no                           |
| 38        | i2s2_mclk_pad_in                 | 0             | no                          | i2s2_mclk_pad_out               | '1'd1                                       | no                           |
| 39        | i2s2_o_ws_pad_in                 | 0             | no                          | i2s2_o_ws_pad_out               | '1'd1                                       | no                           |
| 40        | i2s2_i_sd_pad_in                 | 0             | no                          | i2s2_o_sd_pad_out               | '1'd1                                       | no                           |
| 41        | i2s2_i_bck_pad_in                | 0             | no                          | i2s2_i_bck_pad_out              | '1'd1                                       | no                           |
| 42        | i2s2_i_ws_pad_in                 | 0             | no                          | i2s2_i_ws_pad_out               | '1'd1                                       | no                           |
| 43        | i2s0_i_sd1_pad_in                | 0             | no                          | i2s0_o_sd1_pad_out              | '1'd1                                       | no                           |
| 44        | i2s0_i_sd2_pad_in                | 0             | no                          | spi2_dqs_pad_out                | spi2_dqs_pad_oe                             | yes                          |
| 45        | i2s0_i_sd3_pad_in                | 0             | no                          | spi3_cs2_pad_out                | spi3_cs2_pad_oe                             | no                           |
| 46        | -                                 | -             | -                           | spi3_csi_pad_out                | spi3_csi_pad_oe                             | no                           |
| 47        | spi3_ck_pad_in                   | 0             | no                          | spi3_ck_pad_out                 | spi3_ck_pad_oe                              | no                           |
| 48        | spi3_q_pad_in                    | 0             | no                          | spi3_qo_pad_out                 | spi3_qo_pad_oe                              | no                           |
| 49        | spi3_d_pad_in                    | 0             | no                          | spi3_d_pad_out                  | spi3_d_pad_oe                               | no                           |
| 50        | spi3_hold_pad_in                 | 0             | no                          | spi3_hold_pad_out               | spi3_hold_pad_oe                            | no                           |
| 51        | spi3_wp_pad_in                   | 0             | no                          | spi3_wp_pad_out                 | spi3_wp_pad_oe                              | no                           |
| 52        | spi3_cs_pad_in                   | 0             | no                          | spi3_cs_pad_out                 | spi3_cs_pad_oe                              | no                           |
| 53        | spi2_ck_pad_in                   | 0             | yes                         | spi2_ck_pad_out                 | spi2_ck_pad_oe                              | yes                          |
| 54        | spi2_q_pad_in                    | 0             | yes                         | spi2_q_pad_out                  | spi2_q_pad_oe                               | yes                          |
```