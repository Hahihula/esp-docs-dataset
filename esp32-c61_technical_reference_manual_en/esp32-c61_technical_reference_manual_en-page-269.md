

```markdown
| Signal No. | Input Signal      | Default Value | Direct Input via HP IO MUX | Output Enable Signal when GPIO_FUNCn_OE_SEL = 0 | Direct Output via HP IO MUX |
|------------|-------------------|---------------|----------------------------|--------------------------------------------------|------------------------------|
| 95         | —                 | —             | —                          | —                                                | —                            |
| 96         | —                 | —             | —                          | —                                                | —                            |
| 97         | sig_in_func_97    | 0             | no                         | sig_in_func97                                    | 1'd1                          | no                           |
| 98         | sig_in_func_98    | 0             | no                         | sig_in_func98                                    | 1'd1                          | no                           |
| 99         | sig_in_func_99    | 0             | no                         | sig_in_func99                                    | 1'd1                          | no                           |
| 100        | sig_in_func_100   | 0             | no                         | sig_in_func100                                   | 1'd1                          | no                           |
| 101        | —                 | —             | —                          | —                                                | —                            |
| 102        | —                 | —             | —                          | FSPICS1_out                                      | FSPICS1_oe                    | yes                          |
| 103        | —                 | —             | —                          | FSPICS2_out                                      | FSPICS2_oe                    | yes                          |
| 104        | —                 | —             | —                          | FSPICS3_out                                      | FSPICS3_oe                    | yes                          |
| 105        | —                 | —             | —                          | FSPICS4_out                                      | FSPICS4_oe                    | yes                          |
| 106        | —                 | —             | —                          | FSPICS5_out                                      | FSPICS5_oe                    | yes                          |
| 107        | —                 | —             | —                          | —                                                | —                            |
| 108        | —                 | —             | —                          | —                                                | —                            |
| 109        | —                 | —             | —                          | —                                                | —                            |
| 110        | —                 | —             | —                          | —                                                | —                            |
| 111        | —                 | —             | —                          | —                                                | —                            |
| 112        | —                 | —             | —                          | —                                                | —                            |
| 113        | —                 | —             | —                          | —                                                | —                            |
| 114        | —                 | —             | —                          | —                                                | —                            |
| 115        | —                 | —             | —                          | —                                                | —                            |
| 116        | —                 | —             | —                          | —                                                | —                            |
| 117        | —                 | —             | —                          | —                                                | —                            |
| 118        | —                 | —             | —                          | —                                                | —                            |
| 119        | —                 | —             | —                          | —                                                | —                            |
| 120        | —                 | —             | —                          | —                                                | —                            |
| 121        | —                 | —             | —                          | —                                                | —                            |
| 122        | —                 | —             | —                          | —                                                | —                            |
| 123        | —                 | —             | —                          | —                                                | —                            |
| 124        | —                 | —             | sdio_tohost_int_out        | 1'd1                                              | no                           |
| 125 ~ 255   | —                 | —             | —                          | —                                                | —                            |
```

## 6.13 HP IO MUX Function List

Table 6.13-1 shows the HP IO MUX functions and default states of each HP GPIO pin.
```