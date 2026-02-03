**Title: Appendix A**

**Table Headers:**  
Signal No., Input Signals, Default Value If Unassigned*, Same Input Signal from IO_MUX Core, Output Signals

| Signal No. | Input Signals       | Default Value If Unassigned* | Same Input Signal from IO_MUX Core | Output Signals                   |
|------------|--------------------|------------------------------|-------------------------------------|----------------------------------|
| 34         | pwm0_f0_in         | 0                             | no                                  | pwm0_out1a                       |
| 35         | pwm0_f1_in         | 0                             | no                                  | pwm0_out1b                       |
| 36         | pwm0_f2_in         | 0                             | no                                  | pwm0_out2a                       |
| 37—         | —                  | 0                             | no                                  | pwm0_out2b                       |
| 39         | pcnt_sig_ch0_in0   | 0                             | no                                  | —                                |
| 40         | pcnt_sig_ch1_in0   | 0                             | no                                  | 1'd1                             |
| 41         | pcnt_ctrl_ch0_in0  | 0                             | no                                  | —                                |
| 42         | pcnt_ctrl_ch1_in0  | 0                             | no                                  | 1'd1                             |
| 43         | pcnt_sig_ch0_in1   | 0                             | no                                  | 1'd1                             |
| 44         | pcnt_sig_ch1_in1   | 0                             | no                                  | 1'd1                             |
| 45         | pcnt_ctrl_ch0_in1  | 0                             | no                                  | —                                |
| 46         | pcnt_ctrl_ch1_in1  | 0                             | no                                  | 1'd1                             |
| 47         | pcnt_sig_ch0_in2   | 0                             | no                                  | 1'd1                             |
| 48         | pcnt_sig_ch1_in2   | 0                             | no                                  | —                                |
| 49         | pcnt_ctrl_ch0_in2  | 0                             | no                                  | 1'd1                             |
| 50         | pcnt_ctrl_ch1_in2  | 0                             | no                                  | 1'd1                             |
| 51         | pcnt_sig_ch0_in3   | 0                             | no                                  | —                                |
| 52         | pcnt_sig_ch1_in3   | 0                             | no                                  | 1'd1                             |
| 53         | pcnt_ctrl_ch0_in3  | 0                             | no                                  | 1'd1                             |
| 54         | pcnt_ctrl_ch1_in3  | 0                             | no                                  | —                                |
| 55         | pcnt_sig_ch0_in4   | 0                             | no                                  | 1'd1                             |
| 56         | pcnt_sig_ch1_in4   | 0                             | no                                  | 1'd1                             |
| 57         | pcnt_ctrl_ch0_in4  | 0                             | no                                  | —                                |
| 58         | pcnt_ctrl_ch1_in4  | 0                             | no                                  | 1'd1                             |
| 61         | HSPICS1_in          | 0                             | no                                  | HSPICS1_out                      |
| 62         | HSPICS2_in          | 0                             | no                                  | HSPICS2_out                      |
| 63         | VSPICLK_in          | 0                             | yes                                 | VSPICLK_out_mux                  |
| 64         | VSPIOQ_in           | 0                             | yes                                 | VSPIOQ_out                       |
| 65         | VSPIID_in           | 0                             | yes                                 | VSPIID_out                       |
| 66         | VSPIHD_in           | 0                             | yes                                 | VSPIHD_out                       |
| 67         | VSPWIWP_in          | 0                             | yes                                 | VSPWIWP_out                      |
| 68         | VSPICS0_in          | 0                             | yes                                 | VSPICS0_out                      |
| 69         | VSPICS1_in          | 0                             | no                                  | VSPICS1_out                      |
| 70         | VSPICS2_in          | 0                             | no                                  | VSPICS2_out                      |
| 71         | pcnt_sig_ch0_in5   | 0                             | no                                  | ledc_hs_sig0_out                 |
| 72         | pcnt_sig_ch1_in5   | 0                             | no                                  | ledc_hs_sig1_out                 |
| 73         | pcnt_ctrl_ch0_in5  | 0                             | no                                  | ledc_hs_sig2_out                 |
| 74         | pcnt_ctrl_ch1_in5  | 0                             | no                                  | ledc_hs_sig3_out                 |
| 75         | pcnt_sig_ch0_in6   | 0                             | no                                  | ledc_hs_sig4_out                 |
| 76         | pcnt_sig_ch1_in6   | 0                             | no                                  | ledc_hs_sig5_out                 |

**Footer:**  
Espressif Systems  
Submit Documentation Feedback  
ESP32 Series Datasheet v5.2