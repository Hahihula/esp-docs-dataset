

```markdown
| Signal No. | Input Signal   | Default value | Direct Input via IO MUX | Output Signal     | Output enable signal when GPIO_FUNCn_OEN_SEL = 0 | Direct Output via IO MUX |
|------------|----------------|---------------|--------------------------|-------------------|--------------------------------------------------|---------------------------|
| 52         | rmt_sig_in1    | 0             | no                       | rmt_sig_out1      | 1'd1                                              | no                        |
| 53         | I2CEXTO_SCL_in | 1             | no                       | I2CEXTO_SCL_out   | I2CEXTO_SCL_oe                                   | no                        |
| 54         | I2CEXTO_SDA_in | 1             | no                       | I2CEXTO_SDA_out   | I2CEXTO_SDA_oe                                   | no                        |
| 55         | -              | -             | -                        | gpio_sd0_out      | 1'd1                                              | no                        |
| 56         | -              | -             | -                        | gpio_sd1_out      | 1'd1                                              | no                        |
| 57         | -              | -             | -                        | gpio_sd2_out      | 1'd1                                              | no                        |
| 58         | -              | -             | -                        | gpio_sd3_out      | 1'd1                                              | no                        |
| 59         | -              | -             | -                        | I2SO_SD1_out      | 1'd1                                              | no                        |
| 60         | -              | -             | -                        | -                 | 1'd1                                              | no                        |
| 61         | -              | -             | -                        | -                 | 1'd1                                              | no                        |
| 62         | -              | -             | -                        | -                 | 1'd1                                              | no                        |
| 63         | FSPICLK_in     | 0             | yes                      | FSPICLK_out_mux   | FSPICLK_oe                                       | yes                       |
| 64         | FSPIQ_in       | 0             | yes                      | FSPIQ_out         | FSPIQ_oe                                         | yes                       |
| 65         | FSPID_in       | 0             | yes                      | FSPID_out         | FSPID_oe                                         | yes                       |
| 66         | FSPIHD_in      | 0             | yes                      | FSPIHD_out        | FSPIHD_oe                                        | yes                       |
| 67         | FSPIWP_in      | 0             | yes                      | FSPIWP_out        | FSPIWP_oe                                        | yes                       |
| 68         | FSPICSO_in     | 0             | yes                      | FSPICSO_out       | FSPICSO_oe                                       | yes                       |
| 69         | -              | -             | -                        | FSPICS1_out       | FSPICS1_oe                                       | no                        |
| 70         | -              | -             | -                        | FSPICS2_out       | FSPICS2_oe                                       | no                        |
| 71         | -              | -             | -                        | FSPICS3_out       | FSPICS3_oe                                       | no                        |
| 72         | -              | -             | -                        | FSPICS4_out       | FSPICS4_oe                                       | no                        |
| 73         | -              | -             | -                        | FSPICS5_out       | FSPICS5_oe                                       | no                        |
| 74         | twai_rx        | 1             | no                       | twai_tx            | 1'd1                                              | no                        |
| 75         | -              | -             | -                        | twai_bus_off_on   | 1'd1                                              | no                        |
| 76         | -              | -             | -                        | twai_clkout       | 1'd1                                              | no                        |
| 77         | -              | -             | -                        | -                 | 1'd1                                              | no                        |
| 78         | -              | -             | -                        | -                 | 1'd1                                              | no                        |
```