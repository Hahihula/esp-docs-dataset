

```markdown
| Signal No. | Input Signal      | Default Value | Direct Input via HP IO MUX | Output Signal         | Output Enable Signal when GPIO_FUNCn_OE_SEL = 0 | Direct Output via HP IO MUX |
|------------|-------------------|---------------|----------------------------|------------------------|---------------------------------------------|------------------------------|
| 55         | par1_rx_data7     | 0             | no                         | par1_tx_data7          | 'd1                                         | no                           |
| 56         | FSPICLK_in        | 0             | yes                        | FSPICLK_out_mux        | FSPICLK_oe                                  | yes                          |
| 57         | FSPIQ_in          | 0             | yes                        | FSPIQ_out              | FSPIQ_oe                                    | yes                          |
| 58         | FSPID_in          | 0             | yes                        | FSPID_out              | FSPID_oe                                    | yes                          |
| 59         | FSPIHD_in         | 0             | yes                        | FSPIHD_out             | FSPIHD_oe                                   | yes                          |
| 60         | FSPIWP_in         | 0             | yes                        | FSPIWP_out             | FSPIWP_oe                                   | yes                          |
| 61         | FSPICSO_in        | 0             | yes                        | FSPICSO_out            | FSPICSO_oe                                  | yes                          |
| 62         | par1_rx_clk_in    | 0             | no                         | par1_rx_clk_out        | 'd1                                         | no                           |
| 63         | par1_tx_clk_in    | 0             | no                         | par1_tx_clk_out        | 'd1                                         | no                           |
| 64         | rmt_sig_in0       | 0             | no                         | rmt_sig_out0           | 'd1                                         | no                           |
| 65         | rmt_sig_in1       | 0             | no                         | rmt_sig_out1           | 'd1                                         | no                           |
| 66         | twaiO_rx          | 1             | no                         | twaiO_tx               | 'd1                                         | no                           |
| 67         | —                 | —             | —                          | twaiO_bus_off_on       | 'd1                                         | no                           |
| 68         | —                 | —             | —                          | twaiO_clkout           | 'd1                                         | no                           |
| 69         | —                 | —             | —                          | twaiO_standby          | 'd1                                         | no                           |
| 70         | twai1_rx          | 1             | no                         | twai1_tx               | 'd1                                         | no                           |
| 71         | —                 | —             | —                          | twai1_bus_off_on       | 'd1                                         | no                           |
| 72         | —                 | —             | —                          | twai1_clkout           | 'd1                                         | no                           |
| 73         | —                 | —             | —                          | twai1_standby          | 'd1                                         | no                           |
| 74         | —                 | —             | —                          | —                      | —                                           | —                            |
| 75         | —                 | —             | —                          | —                      | —                                           | —                            |
| 76         | pcnt_rst_in0      | 0             | no                         | gpio_sd0_out           | 'd1                                         | no                           |
| 77         | pcnt_rst_in1      | 0             | no                         | gpio_sd1_out           | 'd1                                         | no                           |
| 78         | pcnt_rst_in2      | 0             | no                         | gpio_sd2_out           | 'd1                                         | no                           |
| 79         | pcnt_rst_in3      | 0             | no                         | gpio_sd3_out           | 'd1                                         | no                           |
| 80         | pwmO_sync0_in     | 0             | no                         | pwmO_out0a             | 'd1                                         | no                           |
| 81         | pwmO_sync1_in     | 0             | no                         | pwmO_out0b             | 'd1                                         | no                           |
| 82         | pwmO_sync2_in     | 0             | no                         | pwmO_out1a             | 'd1                                         | no                           |
```