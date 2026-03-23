

```markdown
12.9.2 Always-on Register Summary                                 437
12.9.3 RTC Timer Register Summary                                  438
12.9.4 Brownout Detector Register Summary                          438
12.10 Registers                                                    440
    12.10.1 PMU Registers                                           440
    12.10.2 Always-on Registers                                      479
    12.10.3 RTC Timer Registers                                      482
    12.10.4 Brownout Detector Registers                              490

13 System Timer (SYSTIMER)                                         496
13.1 Overview                                                      496
13.2 Features                                                      496
13.3 Clock Source Selection                                        497
13.4 Functional Description                                       497
    13.4.1 Counter                                                   498
    13.4.2 Comparator and Alarm                                     498
    13.4.3 Event Task Matrix                                        499
    13.4.4 Synchronization Operation                                 500
    13.4.5 Interrupt                                                501
13.5 Programming Procedure                                         501
    13.5.1 Read Current Count Value                                  501
    13.5.2 Configure One-Time Alarm in Target Mode                   501
    13.5.3 Configure Periodic Alarms in Period Mode                  502
    13.5.4 Update After Light-sleep                                 502
13.6 Register Summary                                               503
13.7 Registers                                                      505

14 Timer Group (TIMG)                                              520
14.1 Overview                                                       520
14.2 Features                                                        520
14.3 Functional Description                                        521
    14.3.1 16-bit Prescaler and Clock Selection                      521
    14.3.2 54-bit Time-base Counter                                  522
    14.3.3 Alarm Generation                                         522
    14.3.4 Timer Reload                                              523
    14.3.5 Event Task Matrix Feature                                 523
    14.3.6 RTC_SLOW_CLK Frequency Calculation                        524
    14.3.7 Interrupts                                                525
14.4 Configuration and Usage                                      525
    14.4.1 Timer as a Simple Clock                                  525
    14.4.2 Timer as One-shot Alarm                                  526
    14.4.3 Timer as Periodic Alarm by APB                           526
    14.4.4 Timer as Periodic Alarm by ETM                            527
    14.4.5 RTC_SLOW_CLK Frequency Calculation                       527
14.5 Register Summary                                               529
14.6 Registers                                                      531
```