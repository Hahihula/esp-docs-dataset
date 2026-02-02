**Table:**

| Signal No. | Input Signals       | Default Value If Unassigned* | Same Input Signal from IO_MUX Core | Output Signals           | Output Enable of Output Signals |
|------------|--------------------|------------------------------|-------------------------------------|--------------------------|---------------------------------|
| 36         | pwm0_f2_in         | 0                            | no                                   | pwm0_out2a              | '1'd1                           |
| 37         | —                   | 0                            | no                                   | pwm0_out2b              | '1'd1                           |
| 39         | pcnt_sig_ch0_in0   | 0                            | no                                   | —                        | '1'd1                           |
| 40         | pcnt_sig_ch1_in0   | 0                            | no                                   | —                        | '1'd1                           |
| 41         | pcnt_ctrl_ch0_in0  | 0                            | no                                   | —                        | '1'd1                           |
| 42         | pcnt_ctrl_ch1_in0  | 0                            | no                                   | —                        | '1'd1                           |
| 43         | pcnt_sig_ch0_in1   | 0                            | no                                   | —                        | '1'd1                           |
| 44         | pcnt_sig_ch1_in1   | 0                            | no                                   | —                        | '1'd1                           |
| 45         | pcnt_ctrl_ch0_in1  | 0                            | no                                   | —                        | '1'd1                           |
| 46         | pcnt_ctrl_ch1_in1  | 0                            | no                                   | —                        | '1'd1                           |
| 47         | pcnt_sig_ch0_in2   | 0                            | no                                   | —                        | '1'd1                           |
| 48         | pcnt_sig_ch1_in2   | 0                            | no                                   | —                        | '1'd1                           |
| 49         | pcnt_ctrl_ch0_in2  | 0                            | no                                   | —                        | '1'd1                           |
| 50         | pcnt_ctrl_ch1_in2  | 0                            | no                                   | —                        | '1'd1                           |
| 51         | pcnt_sig_ch0_in3   | 0                            | no                                   | —                        | '1'd1                           |
| 52         | pcnt_sig_ch1_in3   | 0                            | no                                   | —                        | '1'd1                           |
| 53         | pcnt_ctrl_ch0_in3  | 0                            | no                                   | —                        | '1'd1                           |
| 54         | pcnt_ctrl_ch1_in3  | 0                            | no                                   | —                        | '1'd1                           |
| 55         | pcnt_sig_ch0_in4   | 0                            | no                                   | —                        | '1'd1                           |
| 56         | pcnt_sig_ch1_in4   | 0                            | no                                   | —                        | '1'd1                           |
| 57         | pcnt_ctrl_ch0_in4  | 0                            | no                                   | —                        | '1'd1                           |
| 58         | pcnt_ctrl_ch1_in4  | 0                            | no                                   | —                        | '1'd1                           |
| 61         | HSPICS1_in          | 0                            | no                                   | HSPICS1_out             | HSPICS1_oe                      |
| 62         | HSPICS2_in          | 0                            | no                                   | HSPICS2_out             | HSPICS2_oe                      |
| 63         | VSPICLK_in          | 0                            | yes                                  | VSPICLK_out_mux        | VSPICLK_oe                      |
| 64         | VSPIQ_in            | 0                            | yes                                  | VSPIQ_out               | VSPIQ_oe                        |

**Footer:**
ESP32 TRM (Version 5.9)