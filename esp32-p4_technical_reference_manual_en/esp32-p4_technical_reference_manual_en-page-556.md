

```markdown
| Signal No.| Input Signal                     | Default Value | Direct Input via HP IO MUX | Output Signal                          | Output Enable Signal when GPIO_FUNCn_OE_SEL = 0 | Direct Output via HP IO MUX |
|-----------|-----------------------------------|---------------|----------------------------|----------------------------------------|----------------------------------------------|------------------------------|
| 111       | usb_otg11_avalid_pad_in           | 0             | no                         | usb_otg11_idpullup_pad_out            | 1'd1                                        | no                           |
| 112       | usb_srp_bvalid_pad_in             | 0             | no                         | usb_otg11_dppulldown_pad_out          | 1'd1                                        | no                           |
| 113       | usb_otg11_vbusvalid_pad_in        | 0             | no                         | usb_otg11_dmpulldown_pad_out          | 1'd1                                        | no                           |
| 114       | usb_srp_sessend_pad_in            | 0             | no                         | usb_otg11_drivbus_pad_out             | 1'd1                                        | no                           |
| 115       | -                                 | -             | -                          | usb_srp_chrgvbus_pad_out              | 1'd1                                        | no                           |
| 116       | -                                 | -             | -                          | -                                      | -                                          | -                            |
| 117       | ulpi_clk_pad_in                   | 0             | no                         | -                                      | -                                          | -                            |
| 118       | usb_hsphy_refclk_in               | 0             | no                         | -                                      | -                                          | -                            |
| 119       | -                                 | -             | -                          | -                                      | -                                          | -                            |
| 120       | -                                 | -             | -                          | -                                      | -                                          | -                            |
| 121       | -                                 | -             | -                          | -                                      | -                                          | -                            |
| 122       | -                                 | -             | -                          | -                                      | -                                          | -                            |
| 123       | -                                 | -             | -                          | -                                      | -                                          | -                            |
| 124       | -                                 | -             | -                          | -                                      | -                                          | -                            |
| 125       | -                                 | -             | -                          | -                                      | -                                          | -                            |
| 126       | sd_card_detect_n_1_pad_in         | 0             | no                         | ledc_ls_sig_out_pad_out0              | 1'd1                                        | no                           |
| 127       | sd_card_detect_n_2_pad_in         | 0             | no                         | ledc_ls_sig_out_pad_out1              | 1'd1                                        | no                           |
| 128       | sd_card_int_n_1_pad_in            | 1             | no                         | ledc_ls_sig_out_pad_out2              | 1'd1                                        | no                           |
| 129       | sd_card_int_n_2_pad_in            | 1             | no                         | ledc_ls_sig_out_pad_out3              | 1'd1                                        | no                           |
| 130       | sd_card_write_prt_i_pad_in        | 0             | no                         | ledc_ls_sig_out_pad_out4              | 1'd1                                        | no                           |
| 131       | sd_card_write_prt_2_pad_in        | 0             | no                         | ledc_ls_sig_out_pad_out5              | 1'd1                                        | no                           |
| 132       | sd_data_strobe_1_pad_in           | 0             | no                         | ledc_ls_sig_out_pad_out6              | 1'd1                                        | no                           |
| 133       | sd_data_strobe_2_pad_in           | 0             | no                         | ledc_ls_sig_out_pad_out7              | 1'd1                                        | no                           |
| 134       | i3c_mst_scl_pad_in                | 1             | no                         | i3c_mst_scl_pad_out                   | i3c_mst_scl_oe_pad_out                      | no                           |
| 135       | i3c_mst_sda_pad_in                | 1             | no                         | i3c_mst_sda_pad_out                   | i3c_mst_sda_oe_pad_out                      | no                           |
| 136       | i3c_slv_scl_pad_in                | 1             | no                         | i3c_slv_scl_pad_out                   | i3c_slv_scl_oe_pad_out                      | no                           |
| 137       | i3c_slv_sda_pad_in                | 1             | no                         | i3c_slv_sda_pad_out                   | i3c_slv_sda_oe_pad_out                      | no                           |
```