

```markdown
| Signal No. | Input Signal          | Default value | Direct Input via IO MUX | Output Signal         | Output enable signal when GPIO_FUNCn_OEN_SEL = 0 | Direct Output via IO MUX |
|------------|------------------------|---------------|--------------------------|-----------------------|--------------------------------------------------|---------------------------|
| 54         | parl_rx_data7          | 0             | no                       | parl_tx_data7         | 1'd1                                              | no                        |
| 55         | I2CEXT1_SCL_in         | 1             | no                       | I2CEXT1_SCL_out       | I2CEXT1_SCL_oe                                   | no                        |
| 56         | I2CEXT1_SDA_in         | 1             | no                       | I2CEXT1_SDA_out       | I2CEXT1_SDA_oe                                   | no                        |
| 57         | -                      | -             | -                        | cte_antO              | 1'd1                                              | no                        |
| 58         | -                      | -             | -                        | cte_ant1               | 1'd1                                              | no                        |
| 59         | -                      | -             | -                        | cte_ant2               | 1'd1                                              | no                        |
| 60         | -                      | -             | -                        | cte_ant3               | 1'd1                                              | no                        |
| 61         | -                      | -             | -                        | cte_ant4               | 1'd1                                              | no                        |
| 62         | -                      | -             | -                        | cte_ant5               | 1'd1                                              | no                        |
| 63         | FSPICLK_in             | 0              | yes                      | FSPICLK_out_mux       | FSPICLK_oe                                       | yes                       |
| 64         | FSPIQ_in               | 0              | yes                      | FSPIQ_out             | FSPIQ_oe                                         | yes                       |
| 65         | FSPID_in               | 0              | yes                      | FSPID_out             | FSPID_oe                                         | yes                       |
| 66         | FSPIHD_in              | 0              | yes                      | FSPIHD_out            | FSPIHD_oe                                        | yes                       |
| 67         | FSPIWP_in              | 0              | yes                      | FSPIWP_out            | FSPIWP_oe                                        | yes                       |
| 68         | FSPICSO_in             | 0              | yes                      | FSPICSO_out           | FSPICSO_oe                                       | yes                       |
| 69         | parl_tx_clk_in         | 0              | no                       | parl_rx_clk_out       | 1'd1                                              | no                        |
| 70         | parl_tx_clk_in         | 0              | no                       | parl_tx_clk_out       | 1'd1                                              | no                        |
| 71         | rmt_sig_in0            | 0              | no                       | rmt_sig_out0          | 1'd1                                              | no                        |
| 72         | rmt_sig_in1            | 0              | no                       | rmt_sig_out1          | 1'd1                                              | no                        |
| 73         | twaiO_rx               | 1              | no                       | twaiO_tx               | 1'd1                                              | no                        |
| 74         | -                      | -              | -                        | twaiO_bus_off_on      | 1'd1                                              | no                        |
| 75         | -                      | -              | -                        | twaiO_clkout           | 1'd1                                              | no                        |
| 76         | -                      | -              | -                        | twaiO_standby          | 1'd1                                              | no                        |
| 77         | -                      | -              | -                        | cte_ant6               | 1'd1                                              | no                        |
| 78         | -                      | -              | -                        | cte_ant7               | 1'd1                                              | no                        |
| 79         | -                      | -              | -                        | cte_ant8               | 1'd1                                              | no                        |
| 80         | -                      | -              | -                        | cte_ant9               | 1'd1                                              | no                        |
| 81         | -                      | -              | -                        | -                     | -                                                | -                         |
```