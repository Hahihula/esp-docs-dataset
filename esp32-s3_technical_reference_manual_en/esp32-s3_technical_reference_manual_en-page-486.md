**Table:**

| Signal No. | Input Signal | Default value | Direct Input via IO MUX | Output Signal | Output enable signal when GPIO_FUNCn_OEN_SEL = 0 | Direct Output via IO MUX |
|------------|--------------|---------------|-------------------------|--------------|---------------------------------------------|----------------------------|
| 79         | -            | -             |                        | ledc_ls_sig_out6 | 1'd1                                        | no                          |
| 80         | -            | -             |                        | ledc_ls_sig_out7 | 1'd1                                        | no                          |
| 81         | rmt_sig_in0  | 0             | no                      | rmt_sig_out0     | 1'd1                                        | no                          |
| 82         | rmt_sig_in1  | 0             | no                      | rmt_sig_out1     | 1'd1                                        | no                          |
| 83         | rmt_sig_in2  | 0             | no                      | rmt_sig_out2     | 1'd1                                        | no                          |
| 84         | rmt_sig_in3  | -             |                        | rmt_sig_out3     | 1'd1                                        | no                          |
| 85         | -            | -             |                        | -              | -                                            | -                           |
| 86         | -            | -             |                        | -              | -                                            | -                           |
| 87         | -            | -             |                        | -              | -                                            | -                           |
| 88         | -            | -             |                        | -              | -                                            | -                           |
| 89         | I2CEXTO_SCL_in | 1           | no                      | I2CEXTO_SCL_out | I2CEXTO_SCL_oe | no                          |
| 90         | I2CEXTO_SDA_in | 1           | no                      | I2CEXTO_SDA_out | I2CEXTO_SDA_oe | no                          |
| 91         | I2CEXT1_SCL_in | 1           | no                      | I2CEXT1_SCL_out | I2CEXT1_SCL_oe | no                          |
| 92         | I2CEXT1_SDA_in | 1           | no                      | I2CEXT1_SDA_out | I2CEXT1_SDA_oe | no                          |
| 93         | -            | -             |                        | gpio_sd0_out     | 1'd1                                        | no                          |
| 94         | -            | -             |                        | gpio_sd1_out     | 1'd1                                        | no                          |
| 95         | -            | -             |                        | gpio_sd2_out     | 1'd1                                        | no                          |
| 96         | -            | -             |                        | gpio_sd3_out     | 1'd1                                        | no                          |
| 97         | -            | -             |                        | gpio_sd4_out     | 1'd1                                        | no                          |
| 98         | -            | -             |                        | gpio_sd5_out     | 1'd1                                        | no                          |
| 99         | -            | -             |                        | gpio_sd6_out     | 1'd1                                        | no                          |
| 100        | -            | -             |                        | gpio_sd7_out     | 1'd1                                        | no                          |
| 101        | FSPICLK_in   | 0           | yes                     | FSPICLK_out_mux | FSPICLK_oe | yes                          |
| 102        | FSPIQ_in      | -            | yes                     | FSPIQ_out       | FSPIQ_oe | yes                          |
| 103        | FSPID_in      | 0           | yes                     | FSPID_out       | FSPID_oe | yes                          |
| 104        | FSPIHD_in     | -            | yes                     | FSPIHD_out      | FSPIHD_oe | yes                          |
| 105        | FSPIWP_in     | 0           | yes                     | FSPIWP_out      | FSPIWP_oe | yes                          |

**Footer:**
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback
- GoBack