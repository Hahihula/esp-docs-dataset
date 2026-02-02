**Table: Signal Mapping**

| **Signal No.** | Input Signals | Default Value If Unassigned* | Same Input Signal from IO_MUX Core | Output Signals | Output Enable of Output Signals |
|----------------|---------------|------------------------------|-------------------------------------|----------------|---------------------------------|
| 91             | —             | —                            | rmt_sig_out4                        |                | 'd1'                            |
| 92             | —             | —                            | rmt_sig_out6                        |                | 'd1'                            |
| 94             | twai_rx       | 1                             | no                                   | rmt_sig_out7                          | 'd1'                            |
| 95             | I2CEXT1_SCL_in| 1                             | no                                   | I2CEXT1_SCL_out                        | 'd1'                            |
| 96             | I2CEXT1_SDA_in| 1                             | no                                   | I2CEXT1_SDA_out                        | 'd1'                            |
| 97             | host_card_detect_n_1|0   | 0                                    | host_ccmd_od_pullup_en_n            | 'd1'                            |
| 98             | host_card Detect_n_2|0   | 0                                    | host_rst_n_1                         | 'd1'                            |
| 99             | host_card_write_prt_n_1|0   | 0                                    | host_rst_n_2                         | 'd1'                            |
| 100            | host_card_write_prt_n_2|0   | 0                                    | gpio_sd0_out                          | 'd1'                            |
| 101            | host_card_int_n_1|0    | 0                                    | gpio_sd1_out                          | 'd1'                            |
| 102            | host_card_int_n_2|0    | 0                                    | gpio_sd2_out                          | 'd1'                            |
| 103            | pwm1_sync0_in   | 0                             | no                                   | gpio_sd3_out                          | 'd1'                            |
| 104            | pwm1_sync1_in   | 0                             | no                                   | gpio_sd4_out                          | 'd1'                            |
| 105            | pwm1_sync2_in   | 0                             | no                                   | gpio_sd5_out                          | 'd1'                            |
| 106            | pwm1_f0_in      | 0                             | no                                   | gpio_sd6_out                          | 'd1'                            |
| 107            | pwm1_f1_in      | 0                             | no                                   | gpio_sd7_out                          | 'd1'                            |
| 108            | pwm1_f2_in      | 0                             | no                                   | pwm1_out0a                           | 'd1'                            |
| 109            | pwm0_cap0_in    | 0                             | no                                   | pwm1_out0b                           | 'd1'                            |
| 110            | pwm0_cap1_in    | 0                             | no                                   | pwm1_out1a                           | 'd1'                            |
| 111            | pwm0_cap2_in    | 0                             | no                                   | pwm1_out1b                           | 'd1'                            |
| 112            | pwm1_cap0_in    | 0                             | no                                   | pwm1_out2a                           | 'd1'                            |
| 113            | pwm1_cap1_in    | 0                             | no                                   | pwm1_out2b                           | 'd1'                            |
| 114            | pwm1_cap2_in    | 0                             | no                                   | pwm2_out1h                           | 'd1'                            |
| 115            | pwm2_ffta       | 1                             | no                                   | pwm2_out1l                           | 'd1'                            |
| 116            | pwm2_fttb       | 1                             | no                                   | pwm2_out2h                           | 'd1'                            |
| 117            | pwm2_cap1_in    | 0                             | no                                   | pwm2_out2l                           | 'd1'                            |

*Note: The table includes columns for Signal No., Input Signals, Default Value If Unassigned*, Same Input Signal from IO_MUX Core, Output Signals, and Output Enable of Output Signals. Each row corresponds to a specific signal mapping in the ESP32 TRM (Version 5.0).