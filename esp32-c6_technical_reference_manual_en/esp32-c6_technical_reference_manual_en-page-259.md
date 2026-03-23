

```markdown
| Signal No. | Input Signal       | Default value | Direct Input via IO MUX | Output Signal         | Output enable signal when GPIO_FUNCn_OEN_SEL = 0 | Direct Output via IO MUX |
|------------|--------------------|---------------|--------------------------|------------------------|--------------------------------------------------|---------------------------|
| 54         | parl_rx_data7      | 0             | no                       | parl_tx_data7          | 1'd1                                              | no                        |
| 55         | parl_rx_data8      | 0             | no                       | parl_tx_data8          | 1'd1                                              | no                        |
| 56         | parl_rx_data9      | 0             | no                       | parl_tx_data9          | 1'd1                                              | no                        |
| 57         | parl_rx_data10     | 0             | no                       | parl_tx_data10         | 1'd1                                              | no                        |
| 58         | parl_rx_data11     | 0             | no                       | parl_tx_data11         | 1'd1                                              | no                        |
| 59         | parl_rx_data12     | 0             | no                       | parl_tx_data12         | 1'd1                                              | no                        |
| 60         | parl_rx_data13     | 0             | no                       | parl_tx_data13         | 1'd1                                              | no                        |
| 61         | parl_rx_data14     | 0             | no                       | parl_tx_data14         | 1'd1                                              | no                        |
| 62         | parl_rx_data15     | 0             | no                       | parl_tx_data15         | 1'd1                                              | no                        |
| 63         | FSPICLK_in         | 0             | yes                      | FSPICLK_out_mux        | FSPICLK_oe                                       | yes                       |
| 64         | FSPIQ_in           | 0             | yes                      | FSPIO_out              | FSPIO_oe                                         | yes                       |
| 65         | FSPID_in           | 0             | yes                      | FSPID_out              | FSPID_oe                                         | yes                       |
| 66         | FSPIHD_in          | 0             | yes                      | FSPIHD_out             | FSPIHD_oe                                        | yes                       |
| 67         | FSPIWP_in          | 0             | yes                      | FSPIWP_out             | FSPIWP_oe                                        | yes                       |
| 68         | FSPICSO_in         | 0             | yes                      | FSPICSO_out            | FSPICSO_oe                                       | yes                       |
| 69         | parl_rx_clk_in     | 0             | no                       | sdio_tohost_int_out    | 1'd1                                              | no                        |
| 70         | parl_tx_clk_in     | 0             | no                       | parl_tx_clk_out        | 1'd1                                              | no                        |
| 71         | rmt_sig_in0        | 0             | no                       | rmt_sig_out0           | 1'd1                                              | no                        |
| 72         | rmt_sig_in1        | 0             | no                       | rmt_sig_out1           | 1'd1                                              | no                        |
| 73         | twaiO_rx           | 1             | no                       | twaiO_tx                | 1'd1                                              | no                        |
| 74         | -                  | -             | -                        | twaiO_bus_off_on       | 1'd1                                              | no                        |
| 75         | -                  | -             | -                        | twaiO_clkout           | 1'd1                                              | no                        |
| 76         | -                  | -             | -                        | twaiO_standby          | 1'd1                                              | no                        |
| 77         | twai1_rx           | 1             | no                       | twai1_tx                | 1'd1                                              | no                        |
| 78         | -                  | -             | -                        | twai1_bus_off_on       | 1'd1                                              | no                        |
| 79         | -                  | -             | -                        | twai1_clkout           | 1'd1                                              | no                        |
| 80         | -                  | -             | -                        | twai1_standby          | 1'd1                                              | no                        |
```