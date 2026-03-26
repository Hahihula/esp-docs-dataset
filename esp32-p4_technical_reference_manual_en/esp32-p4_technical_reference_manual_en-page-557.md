

```markdown
| Signal No. | Input Signal                  | Default Value | Direct Input via HP IO MUX | Output Signal                     | Output Enable Signal when GPIO_FUNCn_OE_SEL = 0 | Direct Output via HP IO MUX |
|------------|-------------------------------|---------------|-----------------------------|------------------------------------|----------------------------------------------|------------------------------|
| 138        | -                             | -             | -                           | i3c_mst_scl_pullup_en_pad_out     | 1'd1                                        | no                           |
| 139        | -                             | -             | -                           | i3c_mst_sda_pullup_en_pad_out     | 1'd1                                        | no                           |
| 140        | usb_jtag_tdo_bridge_pad_in    | 0             | no                          | usb_jtag_tdi_bridge_pad_out       | 1'd1                                        | no                           |
| 141        | pcnt_sig_ch0_pad_in0          | 0             | no                          | usb_jtag_tms_bridge_pad_out       | 1'd1                                        | no                           |
| 142        | pcnt_sig_ch0_pad_in1          | 0             | no                          | usb_jtag_tck_bridge_pad_out       | 1'd1                                        | no                           |
| 143        | pcnt_sig_ch0_pad_in2          | 0             | no                          | usb_jtag_trst_bridge_pad_out      | 1'd1                                        | no                           |
| 144        | pcnt_sig_ch0_pad_in3          | 0             | no                          | lcd_cs_pad_out                    | 1'd1                                        | no                           |
| 145        | pcnt_sig_ch1_pad_in0          | 0             | no                          | lcd_dc_pad_out                    | 1'd1                                        | no                           |
| 146        | pcnt_sig_ch1_pad_in1          | 0             | no                          | sd_rst_n_1_pad_out                | 1'd1                                        | no                           |
| 147        | pcnt_sig_ch1_pad_in2          | 0             | no                          | sd_rst_n_2_pad_out                | 1'd1                                        | no                           |
| 148        | pcnt_sig_ch1_pad_in3          | 0             | no                          | sd_ccmd_od_pullup_en_n_pad_out    | 1'd1                                        | no                           |
| 149        | pcnt_ctrl_ch0_pad_in0         | 0             | no                          | lcd_pclk_pad_out                  | 1'd1                                        | no                           |
| 150        | pcnt_ctrl_ch0_pad_in1         | 0             | no                          | cam_clk_pad_out                   | 1'd1                                        | no                           |
| 151        | pcnt_ctrl_ch0_pad_in2         | 0             | no                          | lcd_h_enable_pad_out              | 1'd1                                        | no                           |
| 152        | pcnt_ctrl_ch0_pad_in3         | 0             | no                          | lcd_h_sync_pad_out                | 1'd1                                        | no                           |
| 153        | pcnt_ctrl_ch1_pad_in0         | 0             | no                          | lcd_v_sync_pad_out                | 1'd1                                        | no                           |
| 154        | pcnt_ctrl_ch1_pad_in1         | 0             | no                          | lcd_data_out_pad_out0             | 1'd1                                        | no                           |
| 155        | pcnt_ctrl_ch1_pad_in2         | 0             | no                          | lcd_data_out_pad_out1             | 1'd1                                        | no                           |
| 156        | pcnt_ctrl_ch1_pad_in3         | 0             | no                          | lcd_data_out_pad_out2             | 1'd1                                        | no                           |
| 157        | -                             | -             | -                           | lcd_data_out_pad_out3             | 1'd1                                        | no                           |
| 158        | cam_pclk_pad_in               | 0             | no                          | lcd_data_out_pad_out4             | 1'd1                                        | no                           |
| 159        | cam_h_enable_pad_in           | 0             | no                          | lcd_data_out_pad_out5             | 1'd1                                        | no                           |
| 160        | cam_h_sync_pad_in             | 0             | no                          | lcd_data_out_pad_out6             | 1'd1                                        | no                           |
| 161        | cam_v_sync_pad_in             | 0             | no                          | lcd_data_out_pad_out7             | 1'd1                                        | no                           |
| 162        | cam_data_in_pad_in0           | 0             | no                          | lcd_data_out_pad_out8             | 1'd1                                        | no                           |
| 163        | cam_data_in_pad_in1           | 0             | no                          | lcd_data_out_pad_out9             | 1'd1                                        | no                           |
```