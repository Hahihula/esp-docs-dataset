

```markdown
| Signal No. | Input Signal             | Default Value | Direct Input via HP IO MUX | Output Signal           | Output Enable Signal when GPIO_FUNCn_OE_SEL = 0 | Direct Output via HP IO MUX |
|------------|--------------------------|---------------|----------------------------|-------------------------|---------------------------------------------|------------------------------|
| 83         | twai1_rx_pad_in          | 1             | no                         | twai1_tx_pad_out        | '1'd1                                       | no                            |
| 84         | -                        | -             | -                          | twai1_bus_off_on_pad_out| '1'd1                                       | no                            |
| 85         | -                        | -             | -                          | twai1_clkout_pad_out    | '1'd1                                       | no                            |
| 86         | twai2_rx_pad_in          | 1             | no                         | twai2_tx_pad_out        | '1'd1                                       | no                            |
| 87         | -                        | -             | -                          | twai2_bus_off_on_pad_out| '1'd1                                       | no                            |
| 88         | -                        | -             | -                          | twai2_clkout_pad_out    | '1'd1                                       | no                            |
| 89         | pwmO_sync0_pad_in        | 0             | no                         | pwmO_ch0_a_pad_out      | '1'd1                                       | no                            |
| 90         | pwmO_sync1_pad_in        | 0             | no                         | pwmO_ch0_b_pad_out      | '1'd1                                       | no                            |
| 91         | pwmO_sync2_pad_in        | 0             | no                         | pwmO_ch1_a_pad_out      | '1'd1                                       | no                            |
| 92         | pwmO_f0_pad_in           | 0             | no                         | pwmO_ch1_b_pad_out      | '1'd1                                       | no                            |
| 93         | pwmO_f1_pad_in           | 0             | no                         | pwmO_ch2_a_pad_out      | '1'd1                                       | no                            |
| 94         | pwmO_f2_pad_in           | 0             | no                         | pwmO_ch2_b_pad_out      | '1'd1                                       | no                            |
| 95         | pwmO_cap0_pad_in         | 0             | no                         | pwm1_ch0_a_pad_out      | '1'd1                                       | no                            |
| 96         | pwmO_cap1_pad_in         | 0             | no                         | pwm1_ch0_b_pad_out      | '1'd1                                       | no                            |
| 97         | pwmO_cap2_pad_in         | 0             | no                         | pwm1_ch1_a_pad_out      | '1'd1                                       | no                            |
| 98         | pwm1_sync0_pad_in        | 0             | no                         | pwm1_ch1_b_pad_out      | '1'd1                                       | no                            |
| 99         | pwm1_sync1_pad_in        | 0             | no                         | pwm1_ch2_a_pad_out      | '1'd1                                       | no                            |
| 100        | pwm1_sync2_pad_in        | 0             | no                         | pwm1_ch2_b_pad_out      | '1'd1                                       | no                            |
| 101        | pwm1_f0_pad_in           | 0             | no                         | -                       | -                                           | -                              |
| 102        | pwm1_f1_pad_in           | 0             | no                         | -                       | -                                           | -                              |
| 103        | pwm1_f2_pad_in           | 0             | no                         | -                       | -                                           | -                              |
| 104        | pwm1_cap0_pad_in         | 0             | no                         | -                       | -                                           | -                              |
| 105        | pwm1_cap1_pad_in         | 0             | no                         | twaiO_standby_pad_out   | '1'd1                                       | no                            |
| 106        | pwm1_cap2_pad_in         | 0             | no                         | twai1_standby_pad_out   | '1'd1                                       | no                            |
| 107        | gmii_mdi_pad_in           | 0             | no                         | twai2_standby_pad_out   | '1'd1                                       | no                            |
| 108        | gmac_phy_col_pad_in      | 0             | no                         | gmii_mdc_pad_out         | '1'd1                                       | no                            |
| 109        | gmac_phy_crs_pad_in      | 0             | no                         | gmii_mdo_pad_out         | gmii_mdo_oe_pad_out                         | no                            |
| 110        | usb_otg11_iddig_pad_in    | 0             | no                         | usb_srp_dischargbus_pad_out | '1'd1                                       | no                            |
```