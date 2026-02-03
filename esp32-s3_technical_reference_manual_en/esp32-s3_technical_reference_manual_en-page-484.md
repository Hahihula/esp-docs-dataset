**Table:**

| Signal No. | Input Signal       | Default value | Direct Input via IO MUX | Output Signal         | Output enable signal when GPIO_FUNCn_OEN_SEL = 0 | Direct Output via IO MUX |
|------------|--------------------|---------------|-------------------------|-----------------------|--------------------------------------------------|----------------------------|
| 25         | I2S0I_SD_in        | O             | no                      | I2S0O_SD_out          | 1'd1                                             | no                         |
| 26         | I2S0I_BCK_in       | O             | no                      | I2S0I_BCK_out         | 1'd1                                             | no                         |
| 27         | I2S0I_WS_in        | O             | no                      | I2S0I_WS_out          | 1'd1                                             | no                         |
| 28         | I2S1O_BCK_in       | O             | no                      | I2S1O_BCK_out         | 1'd1                                             | no                         |
| 29         | I2S1O_WS_in        | O             | no                      | I2S1O_WS_out          | 1'd1                                             | no                         |
| 30         | I2S1I_SD_in        | O             | no                      | I2S1SD_OUT            | 1'd1                                             | no                         |
| 31         | I2S1I_BCK_in       | O             | no                      | I2S1IBCK_OUT          | 1'd1                                             | no                         |
| 32         | I2S1I_WS_in        | O             | no                      | I2S1I_WS_out          | 1'd1                                             | no                         |
| 33         | pcnt_sig_ch0_in0   | O             | -                       | -                     | 1'd1                                             | no                         |
| 34         | pcnt_sig_ch1_in0   | O             | -                       | -                     | 1'd1                                             | no                         |
| 35         | pcnt_ctrl_ch0_in0  | O             | -                       | -                     | 1'd1                                             | -                          |
| 36         | pcnt_ctrl_ch1_in0  | O             | -                       | -                     | 1'd1                                             | -                          |
| 37         | pcnt_sig_ch0_in1   | O             | no                      | -                     | 1'd1                                             | -                          |
| 38         | pcnt_sig_ch1_in1   | O             | no                      | -                     | 1'd1                                             | -                          |
| 39         | pcnt_ctrl_ch0_in1  | O             | no                      | -                     | 1'd1                                             | -                          |
| 40         | pcnt_ctrl_ch1_in1  | O             | no                      | -                     | 1'd1                                             | -                          |
| 41         | pcnt_sig_ch0_in2   | O             | no                      | -                     | 1'd1                                             | -                          |
| 42         | pcnt_sig_ch1_in2   | O             | no                      | -                     | 1'd1                                             | -                          |
| 43         | pcnt_ctrl_ch0_in2  | O             | no                      | -                     | 1'd1                                             | -                          |
| 44         | pcnt_ctrl_ch1_in2  | O             | no                      | -                     | 1'd1                                             | -                          |
| 45         | pcnt_sig_ch0_in3   | O             | no                      | -                     | 1'd1                                             | -                          |
| 46         | pcnt_sig_ch1_in3   | O             | no                      | -                     | 1'd1                                             | -                          |
| 47         | pcnt_ctrl_ch0_in3  | O             | no                      | -                     | 1'd1                                             | -                          |
| 48         | pcnt_ctrl_ch1_in3  | O             | no                      | -                     | 1'd1                                             | -                          |
| 49         | -                   | -             | -                       | -                     | 1'd1                                             | -                          |
| 50         | -                   | -             | -                       | -                     | 1'd1                                             | -                          |
| 51         | I2S0I_SD_in        | O             | no                      | -                     | 1'd1                                             | -                          |

**Side Text:**
- ESP32-S3 TRM (Version 1.7)
- GoBack
- Submit Documentation Feedback

**Header:**
- Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)