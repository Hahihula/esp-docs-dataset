

```markdown
33.2.2.2 Error and Overload Frames                                 1069
33.2.2.3 Interframe Space                                         1071
33.2.3 TWAI Errors                                                1071
   33.2.3.1 Error Types                                           1071
   33.2.3.2 Error States                                          1072
   33.2.3.3 Error Counters                                        1072
33.2.4 TWAI Bit Timing                                            1073
   33.2.4.1 Nominal Bit                                           1073
   33.2.4.2 Hard Synchronization and Resynchronization             1074
33.3 Architectural Overview                                       1075
33.3.1 Registers Block                                            1075
33.3.2 Bit Stream Processor                                       1076
33.3.3 Error Management Logic                                     1076
33.3.4 Bit Timing Logic                                           1077
33.3.5 Acceptance Filter                                          1077
33.3.6 Receive FIFO                                               1077
33.4 Functional Description                                       1077
33.4.1 Modes                                                      1077
   33.4.1.1 Reset Mode                                            1077
   33.4.1.2 Operation Mode                                        1077
33.4.2 Bit Timing                                                 1078
33.4.3 Interrupt Management                                       1079
   33.4.3.1 Receive Interrupt (RXI)                                1079
   33.4.3.2 Transmit Interrupt (TXI)                               1079
   33.4.3.3 Error Warning Interrupt (EWI)                          1080
   33.4.3.4 Data Overrun Interrupt (DOI)                           1080
   33.4.3.5 Error Passive Interrupt (TXI)                          1080
   33.4.3.6 Arbitration Lost Interrupt (ALI)                       1080
   33.4.3.7 Bus Error Interrupt (BEI)                              1080
   33.4.3.8 Bus Idle Status Interrupt (BISI)                       1081
33.4.4 Transmit and Receive Buffers                               1081
   33.4.4.1 Overview of Buffers                                   1081
   33.4.4.2 Frame Information                                     1082
   33.4.4.3 Frame Identifier                                      1082
   33.4.4.4 Frame Data                                            1083
33.4.5 Receive FIFO and Data Overruns                             1083
33.4.6 Acceptance Filter                                          1084
   33.4.6.1 Single Filter Mode                                    1085
   33.4.6.2 Dual Filter Mode                                      1085
33.4.7 Error Management                                           1086
   33.4.7.1 Error Warning Limit                                   1087
   33.4.7.2 Error Passive                                         1087
   33.4.7.3 Bus-Off and Bus-Off Recovery                          1087
33.4.8 Error Code Capture                                        1088
33.4.9 Arbitration Lost Capture                                   1089
33.4.10 Transceiver Auto-Standby                                  1090
```