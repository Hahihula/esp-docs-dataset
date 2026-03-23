

```markdown
| Signal No. | Input Signal          | Default value | Direct Input via IO MUX | Output Signal           | Output enable signal when GPIO_FUNCn_OEN_SEL = 0 | Direct Output via IO MUX |
|------------|-----------------------|---------------|--------------------------|-------------------------|---------------------------------------------|----------------------------|
| 25         | -                     | -             | -                        | -                       | 1'd1                                         | no                          |
| 26         | -                     | -             | -                        | -                       | 1'd1                                         | no                          |
| 27         | -                     | -             | -                        | -                       | 1'd1                                         | no                          |
| 28         | cpu_gpio_in0          | 0             | no                       | cpu_gpio_out0           | cpu_gpio_out_oen0                            | no                          |
| 29         | cpu_gpio_in1          | 0             | no                       | cpu_gpio_out1           | cpu_gpio_out_oen1                            | no                          |
| 30         | cpu_gpio_in2          | 0             | no                       | cpu_gpio_out2           | cpu_gpio_out_oen2                            | no                          |
| 31         | cpu_gpio_in3          | 0             | no                       | cpu_gpio_out3           | cpu_gpio_out_oen3                            | no                          |
| 32         | cpu_gpio_in4          | 0             | no                       | cpu_gpio_out4           | cpu_gpio_out_oen4                            | no                          |
| 33         | cpu_gpio_in5          | 0             | no                       | cpu_gpio_out5           | cpu_gpio_out_oen5                            | no                          |
| 34         | cpu_gpio_in6          | 0             | no                       | cpu_gpio_out6           | cpu_gpio_out_oen6                            | no                          |
| 35         | cpu_gpio_in7          | 0             | no                       | cpu_gpio_out7           | cpu_gpio_out_oen7                            | no                          |
| 36         | -                     | -             | -                        | usb_jtag_tck            | 1'd1                                         | no                          |
| 37         | -                     | -             | -                        | usb_jtag_tms            | 1'd1                                         | no                          |
| 38         | -                     | -             | -                        | usb_jtag_tdi            | 1'd1                                         | no                          |
| 39         | -                     | -             | -                        | usb_jtag_tdo            | 1'd1                                         | no                          |
| 40         | -                     | -             | -                        | -                       | 1'd1                                         | no                          |
| 41         | -                     | -             | -                        | -                       | 1'd1                                         | no                          |
| 42         | -                     | -             | -                        | -                       | 1'd1                                         | no                          |
| 43         | -                     | -             | -                        | -                       | 1'd1                                         | no                          |
| 44         | -                     | -             | -                        | -                       | 1'd1                                         | no                          |
| 45         | ext_adc_start         | 0             | no                       | ledc_ls_sig_out0        | 1'd1                                         | no                          |
| 46         | -                     | -             | -                        | ledc_ls_sig_out1        | 1'd1                                         | no                          |
| 47         | -                     | -             | -                        | ledc_ls_sig_out2        | 1'd1                                         | no                          |
| 48         | -                     | -             | -                        | ledc_ls_sig_out3        | 1'd1                                         | no                          |
| 49         | -                     | -             | -                        | ledc_ls_sig_out4        | 1'd1                                         | no                          |
| 50         | -                     | -             | -                        | ledc_ls_sig_out5        | 1'd1                                         | no                          |
| 51         | rmt_sig_in0           | 0             | no                       | rmt_sig_out0            | 1'd1                                         | no                          |
```