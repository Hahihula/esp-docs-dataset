

```markdown
| Signal No. | Input Signal      | Default Value | Direct Input via HP IO MUX | Output Signal   | Output Enable Signal when GPIO_FUNCn_OE_SEL = 0 | Direct Output via HP IO MUX |
|------------|-------------------|---------------|----------------------------|-----------------|--------------------------------------------------|------------------------------|
| 7          | UOCTS_in          | 0             | no                         | UARTS_out       | 1'd1                                              | no                           |
| 8          | UODSR_in          | 0             | no                         | UODTR_out       | 1'd1                                              | no                           |
| 9          | U1RXD_in          | 1             | no                         | U1TXD_out       | 1'd1                                              | no                           |
| 10         | U1CTS_in          | 0             | no                         | U1RTS_out       | 1'd1                                              | no                           |
| 11         | U1DSR_in          | 0             | no                         | U1DTR_out       | 1'd1                                              | no                           |
| 12         | I2S_MCLK_in       | 0             | no                         | I2S_MCLK_out    | 1'd1                                              | no                           |
| 13         | I2SO_BCK_in       | 0             | no                         | I2SO_BCK_out    | 1'd1                                              | no                           |
| 14         | I2SO_WS_in        | 0             | no                         | I2SO_WS_out     | 1'd1                                              | no                           |
| 15         | I2SI_SD_in        | 0             | no                         | I2SO_SD_out     | 1'd1                                              | no                           |
| 16         | I2SI_BCK_in       | 0             | no                         | I2SI_BCK_out    | 1'd1                                              | no                           |
| 17         | I2SI_WS_in        | 0             | no                         | I2SI_WS_out     | 1'd1                                              | no                           |
| 18         | —                 | —             | —                          | I2SO_SD1_out    | 1'd1                                              | no                           |
| 19         | —                 | —             | —                          | —               | —                                                | —                            |
| 20         | —                 | —             | —                          | —               | —                                                | —                            |
| 21         | —                 | —             | —                          | —               | —                                                | —                            |
| 22         | —                 | —             | —                          | —               | —                                                | —                            |
| 23         | —                 | —             | —                          | —               | —                                                | —                            |
| 24         | —                 | —             | —                          | —               | —                                                | —                            |
| 25         | —                 | —             | —                          | —               | —                                                | —                            |
| 26         | —                 | —             | —                          | —               | —                                                | —                            |
| 27         | cpu_gpio_in0      | 0             | no                         | cpu_gpio_out0   | cpu_gpio_out_oen0                               | no                           |
| 28         | cpu_gpio_in1      | 0             | no                         | cpu_gpio_out1   | cpu_gpio_out_oen1                               | no                           |
| 29         | cpu_gpio_in2      | 0             | no                         | cpu_gpio_out2   | cpu_gpio_out_oen2                               | no                           |
| 30         | cpu_gpio_in3      | 0             | no                         | cpu_gpio_out3   | cpu_gpio_out_oen3                               | no                           |
| 31         | cpu_gpio_in4      | 0             | no                         | cpu_gpio_out4   | cpu_gpio_out_oen4                               | no                           |
| 32         | cpu_gpio_in5      | 0             | no                         | cpu_gpio_out5   | cpu_gpio_out_oen5                               | no                           |
| 33         | cpu_gpio_in6      | 0             | no                         | cpu_gpio_out6   | cpu_gpio_out_oen6                               | no                           |
| 34         | cpu_gpio_in7      | 0             | no                         | cpu_gpio_out7   | cpu_gpio_out_oen7                               | no                           |
| 35         | usb_jtag_tdo      | 0             | no                         | —               | —                                                | —                            |
| 36         | —                 | —             | —                          | —               | —                                                | —                            |
| 37         | —                 | —             | —                          | —               | —                                                | —                            |
| 38         | —                 | —             | —                          | —               | —                                                | —                            |
| 39         | —                 | —             | —                          | —               | —                                                | —                            |
| 40         | —                 | —             | —                          | —               | —                                                | —                            |
| 41         | —                 | —             | —                          | —               | —                                                | —                            |
| 42         | —                 | —             | —                          | —               | —                                                | —                            |
| 43         | —                 | —             | —                          | —               | —                                                | —                            |
| 44         | —                 | —             | —                          | —               | —                                                | —                            |
| 45         | —                 | —             | —                          | —               | —                                                | —                            |
| 46         | I2CEXT0_SCL_in    | 1             | no                         | I2CEXT0_SCL_out | I2CEXT0_SCL_oe                                   | no                           |
| 47         | I2CEXT0_SDA_in    | 1             | no                         | I2CEXT0_SDA_out | I2CEXT0_SDA_oe                                   | no                           |
| 48         | —                 | —             | —                          | —               | —                                                | —                            |
| 49         | —                 | —             | —                          | —               | —                                                | —                            |
| 50         | —                 | —             | —                          | —               | —                                                | —                            |
```