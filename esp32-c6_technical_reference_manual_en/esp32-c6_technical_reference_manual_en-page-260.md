

```markdown
| Signal No. | Input Signal         | Default value | Direct Input via IO MUX | Output Signal     | Output enable signal when GPIO_FUNCn_OEN_SEL = 0 | Direct Output via IO MUX |
|------------|----------------------|---------------|--------------------------|-------------------|--------------------------------------------------|---------------------------|
| 81         | -                    | -             | -                        | -                 | -                                                | -                         |
| 82         | -                    | -             | -                        | -                 | -                                                | -                         |
| 83         | -                    | -             | -                        | gpio_sd0_out      | 1'd1                                             | no                        |
| 84         | -                    | -             | -                        | gpio_sd1_out      | 1'd1                                             | no                        |
| 85         | -                    | -             | -                        | gpio_sd2_out      | 1'd1                                             | no                        |
| 86         | -                    | -             | -                        | gpio_sd3_out      | 1'd1                                             | no                        |
| 87         | pwm0_sync0_in        | 0             | no                       | pwm0_outOa        | 1'd1                                             | no                        |
| 88         | pwm0_sync1_in        | 0             | no                       | pwm0_outOb        | 1'd1                                             | no                        |
| 89         | pwm0_sync2_in        | 0             | no                       | pwm0_out1a        | 1'd1                                             | no                        |
| 90         | pwm0_f0_in           | 0             | no                       | pwm0_out1b        | 1'd1                                             | no                        |
| 91         | pwm0_f1_in           | 0             | no                       | pwm0_out2a        | 1'd1                                             | no                        |
| 92         | pwm0_f2_in           | 0             | no                       | pwm0_out2b        | 1'd1                                             | no                        |
| 93         | pwm0_cap0_in         | 0             | no                       | -                 | -                                                | -                         |
| 94         | pwm0_cap1_in         | 0             | no                       | -                 | -                                                | -                         |
| 95         | pwm0_cap2_in         | 0             | no                       | -                 | -                                                | -                         |
| 96         | -                    | -             | -                        | -                 | -                                                | -                         |
| 97         | sig_in_func_97        | 0             | no                       | sig_in_func97     | 1'd1                                             | no                        |
| 98         | sig_in_func_98        | 0             | no                       | sig_in_func98     | 1'd1                                             | no                        |
| 99         | sig_in_func_99        | 0             | no                       | sig_in_func99     | 1'd1                                             | no                        |
| 100        | sig_in_func_100       | 0             | no                       | sig_in_func100    | 1'd1                                             | no                        |
| 101        | pcnt_sig_ch0_in0      | 0             | no                       | FSPICS1_out       | FSPICS1_oe                                      | yes                       |
| 102        | pcnt_sig_ch1_in0      | 0             | no                       | FSPICS2_out       | FSPICS2_oe                                      | yes                       |
| 103        | pcnt_ctrl_ch0_in0     | 0             | no                       | FSPICS3_out       | FSPICS3_oe                                      | yes                       |
| 104        | pcnt_ctrl_ch1_in0     | 0             | no                       | FSPICS4_out       | FSPICS4_oe                                      | yes                       |
| 105        | pcnt_sig_ch0_in1      | 0             | no                       | FSPICS5_out       | FSPICS5_oe                                      | yes                       |
| 106        | pcnt_sig_ch1_in1      | 0             | no                       | -                 | -                                                | -                         |
| 107        | pcnt_ctrl_ch0_in1     | 0             | no                       | -                 | -                                                | -                         |
| 108        | pcnt_ctrl_ch1_in1     | 0             | no                       | -                 | -                                                | -                         |
```