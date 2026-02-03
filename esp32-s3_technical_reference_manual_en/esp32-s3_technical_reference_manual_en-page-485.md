**Table:**

| Signal No. | Input Signal       | Default value | Direct Input via IO MUX | Output Signal         | Output enable signal when GPIO_FUNCn_OEN_SEL = 0 | Direct Output via IO MUX |
|------------|--------------------|---------------|-------------------------|-----------------------|--------------------------------------------------|----------------------------|
| 52         | I2S0I_SD2_in       | O             | no                      | -                    | 1'd1                                              | -                          |
| 53         | I2S0I_SD3_in       | O             | no                      | -                    | 1'd1                                              | -                          |
| 54         | Core1_gpio_in7     | O             | no                      | Core1_gpio_out7      | 1'd1                                              | no                         |
| 55         | -                   | -             | -                       | -                    | 1'd1                                              | -                          |
| 56         | -                   | -             | -                       | -                    | 1'd1                                              | -                          |
| 57         | -                   | -             | -                       | -                    | 1'd1                                              | -                          |
| 58         | usb_otg_iddig_in   | O             | no                      | -                    | 1'd1                                              | -                          |
| 59         | usb_otg_avolid_in  | O             | no                      | -                    | 1'd1                                              | -                          |
| 60         | usb_srp_bvalid_in  | O             | no                      | usb_otg_idpullup     | 1'd1                                              | no                         |
| 61         | usb_otg_vbusvalid_in | O        | no                      | usb_otg_dppulldown   | 1'd1                                              | no                         |
| 62         | usb_srp_sessend_in | O             | no                      | usb_otg_dmpulldown   | 1'd1                                              | no                         |
| 63         | -                   | -             | -                       | -                    | 1'd1                                              | no                         |
| 64         | -                   | -             | -                       | -                    | 1'd1                                              | no                         |
| 65         | -                   | -             | -                       | -                    | 1'd1                                              | no                         |
| 66         | SPI3_CLK_in        | O             | no                      | SPI3_CLK_out_mux    | SPI3_CLK_oe                                     | no                         |
| 67         | SPI3_Q_in          | O             | no                      | SPI3_Q_out           | SPI3_Q_oe                                      | no                         |
| 68         | SPI3_D_in          | -             | -                       | SPI3_D_out           | SPI3_D_oe                                      | no                         |
| 69         | SPI3_HD_in         | O             | no                      | SPI3_HD_out          | SPI3_HD_oe                                     | no                         |
| 70         | SPI3_WP_in         | -             | -                       | SPI3_WP_out          | SPI3_WP_oe                                     | no                         |
| 71         | SPI3_CS0_in        | O             | no                      | SPI3_CS0_out         | SPI3_CS0_oe                                    | no                         |
| 72         | -                   | -             | -                       | SPI3_CS1_out         | SPI3_CS1_oe                                    | no                         |
| 73         | ext_adc_start      | O             | no                      | ledc_ls_sig_out0     | 1'd1                                              | no                         |
| 74         | -                   | -             | -                       | ledc_ls_sig_out1     | 1'd1                                              | no                         |
| 75         | -                   | -             | -                       | ledc_ls_sig_out2     | 1'd1                                              | no                         |
| 76         | -                   | -             | -                       | ledc_ls_sig_out3     | 1'd1                                              | no                         |
| 77         | -                   | -             | -                       | ledc_ls_sig_out4     | 1'd1                                              | no                         |
| 78         | -                   | -             | -                       | ledc_ls_sig_out5     | 1'd1                                              | no                         |

**Footer:**
- ESP32-S3 TRM (Version 1.0)
- GoBack

(Note: The text "ESP32-S3 TRM" is part of the footer, indicating that this table might be from a technical reference manual for an ESP32-S3 chip.)