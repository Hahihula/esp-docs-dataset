**Table:**

| Signal No. | Input Signal       | Default value | Direct Input via IO MUX | Output Signal           | Output enable signal when GPIO_FUNCn_OEN_SEL = 0 | Direct Output via IO MUX |
|------------|--------------------|---------------|-------------------------|-------------------------|--------------------------------------------------|----------------------------|
| 160        | pwm0_sync0_in     | 0             | no                      | pwm0_out0a              | 1'd1                                             | no                          |
| 161        | pwm0_sync1_in     | 0             | no                      | pwm0_out0b              | 1'd1                                             | no                          |
| 162        | pwm0_sync2_in     | 0             | no                      | pwm0_out1a              | 1'd1                                             | no                          |
| 163        | pwm0_f0_in        | 0             | no                      | pwm0_out1b              | 1'd1                                             | no                          |
| 164        | pwm0_f1_in        | 0             | no                      | pwm0_out2a              | 1'd1                                             | no                          |
| 165        | pwm0_f2_in        | 0             | no                      | pwm0_out2b              | 1'd1                                             | no                          |
| 166        | pwm0_cap0_in      | 0             | no                      | pwm1_out0a              | 1'd1                                             | no                          |
| 167        | pwm0_cap1_in      | 0             | no                      | pwm1_out0b              | 1'd1                                             | no                          |
| 168        | pwm0_cap2_in      | 0             | no                      | pwm1_out1a              | 1'd1                                             | no                          |
| 169        | pwm1_sync0_in     | 0             | no                      | pwm1_out1b              | 1'd1                                             | no                          |
| 170        | pwm1_sync1_in     | 0             | no                      | pwm1_out2a              | 1'd1                                             | no                          |
| 171        | pwm1_sync2_in     | 0             | no                      | pwm1_out2b              | 1'd1                                             | no                          |
| 172        | pwm1_f0_in        | 0             | no                      | sdhost_clk_out_1       | 1'd1                                             | no                          |
| 173        | pwm1_f1_in        | 0             | no                      | sdhost_clk_out_2       | 1'd1                                             | no                          |
| 174        | pwm1_f2_in        | 0             | no                      | sdhost_rst_n_1         | 1'd1                                             | no                          |
| 175        | pwm1_cap0_in      | 0             | no                      | sdhost_rst_n_2         | 1'd1                                             | no                          |
| 176        | pwm1_cap1_in      | 0             | host_ccmd_od_pullup_en_n |                    | sdo_host_int_out_rut | no                          |
| 177        | pwm1_cap2_in      | 0             | sdo_host_int_out_rut   | sdo_host_int_out_1     | sdo_host_ccmd_out_en_1 | no                          |
| 178        | sdhost_ccmd_in_1  | 1             | sdo_host_int_out_1     | sdo_host_ccmd_out_en_2 | sdo_host_ccmd_out_en_2 | no                          |
| 179        | sdhost_ccmd_in_2  | 1             | sdo_host_int_out_2     | sdo_host_ccmd_out_en_3 | sdo_host_ccmd_out_en_3 | no                          |
| 180        | sdhost_cdata_in_10| 1             | sdo_host_int_out_3     | sdo_host_ccmd_out_en_4 | sdo_host_ccmd_out_en_4 | no                          |
| 181        | sdhost_cdata_in_12| 1             | sdo_host_int_out_5     | sdo_host_ccmd_out_en_5 | sdo_host_ccmd_out_en_5 | no                          |
| 182        | sdhost_cdata_in_13| 1             | sdo_host_int_out_6     | sdo_host_ccmd_out_en_6 | sdo_host_ccmd_out_en_6 | no                          |
| 183        | sdhost_cdata_in_14| 1             | sdo_host_int_out_7     | sdo_host_ccmd_out_en_7 | sdo_host_ccmd_out_en_7 | no                          |
| 184        | sdhost_cdata_in_15| 1             | sdo_host_int_out_8     | sdo_host_ccmd_out_en_8 | sdo_host_ccmd_out_en_8 | no                          |

**Footer:**
- ESP32-S2 TRM (Version 1.7)
- Submit Documentation Feedback
- GoBack