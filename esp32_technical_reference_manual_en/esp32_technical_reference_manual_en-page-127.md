**Table:**

| Signal No. | Input Signals       | Default Value If Unassigned* | Same Input Signal from IO_MUX Core | Output Signals                   | Output Enable of Output Signals |
|------------|--------------------|------------------------------|-------------------------------------|-----------------------------------|---------------------------------|
| 65         | VSPID_in           | 0                             | yes                                 | VSPID_out                         | VSPID_oe                        |
| 66         | VSPIHD_in          | 0                             | yes                                 | VSPIHD_out                       | VSPIHD_oe                      |
| 67         | VSPIWP_in          | 0                             | yes                                 | VSPIWP_out                       | VSPIWP_oe                      |
| 68         | VSPICSO_in         | 0                             | yes                                 | VSPICSO_out                      | VSPICSO_oe                     |
| 69         | VSPICS1_in         | no                            |                                     | VSPICS1_out                       | VSPICS1_oe                     |
| 70         | VSPICS2_in         | 0                             | no                                  | VSPICS2_out                       | VSPICS2_oe                     |
| 71         | pcnt_sig_ch0_in5   | 0                             |                                     | ledc_hs_sig_out0                  | 'd1'                            |
| 72         | pcnt_sig_ch1_in5   | 0                             |                                     | ledc_hs_sig_out1                  | 'd1'                            |
| 73         | pcnt_ctrl_ch0_in5  | 0                             |                                     | ledc_hs_sig_out2                  | 'd1'                            |
| 74         | pcnt_ctrl_ch1_in5  | 0                             |                                     | ledc_hs_sig_out3                  | 'd1'                            |
| 75         | pcnt_sig_ch0_in6   | 0                             |                                     | ledc_hs_sig_out4                  | 'd1'                            |
| 76         | pcnt_sig_ch1_in6   | 0                             |                                     | ledc_hs_sig_out5                  | 'd1'                            |
| 77         | pcnt_ctrl_ch0_in6  | 0                             |                                     | ledc_hs_sig_out6                  | 'd1'                            |
| 78         | pcnt_ctrl_ch1_in6  | 0                             |                                     | ledc_hs_sig_out7                  | 'd1'                            |
| 79         | pcnt_sig_ch0_in7   | 0                             |                                     | ledc_ls_sig_out0                  | 'd1'                            |
| 80         | pcnt_sig_ch1_in7   | 0                             |                                     | ledc_ls_sig_out1                  | 'd1'                            |
| 81         | pcnt_ctrl_ch0_in7  | 0                             |                                     | ledc_ls_sig_out2                  | 'd1'                            |
| 82         | pcnt_ctrl_ch1_in7  | 0                             |                                     | ledc_ls_sig_out3                  | 'd1'                            |
| 83         | rmt_sig_in0        | 0                             |                                     | rmt_sig_out0                      | 'd1'                            |
| 84         | rmt_sig_in1        | 0                             |                                     | rmt_sig_out1                      | 'd1'                            |
| 85         | rmt_sig_in2        | 0                             |                                     | rmt_sig_out2                      | 'd1'                            |
| 86         | rmt_sig_in3        | 0                             |                                     | rmt_sig_out3                      | 'd1'                            |
| 87         | rmt_sig_in4        | 0                             |                                     | rmt_sig_out4                      | 'd1'                            |
| 88         | rmt_sig_in5        | 0                             |                                     | rmt_sig_out5                      | 'd1'                            |
| 89         | rmt_sig_in6        | 0                             |                                     | rmt_sig_out6                      | 'd1'                            |
| 90         | rmt_sig_in7        | 0                             |                                     | rmt_sig_out7                      | 'd1'                            |

*Note: The table includes a note about the default value if unassigned, but it is not explicitly stated in all rows.