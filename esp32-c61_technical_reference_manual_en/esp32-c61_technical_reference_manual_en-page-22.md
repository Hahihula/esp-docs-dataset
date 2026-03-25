

```markdown
28.10.2.5 A-law/μ-law Compression and Decompression                                 1040

28.11 Event Task Matrix Feature                                                        1041
28.12 I2S Interrupts                                                                  1041
28.13 Software Configuration Process                                                    1042
   28.13.1 Configure I2S as TX Mode                                                     1042
   28.13.2 Configure I2S as RX Mode                                                     1043
28.14 Register Summary                                                                 1044
28.15 Registers                                                                        1045

29 USB Serial/JTAG Controller                                                          1062
29.1 Overview                                                                          1062
29.2 Feature List                                                                      1062
29.3 Functional Description                                                            1064
   29.3.1 CDC-ACM USB Interface Functional Description                                  1064
   29.3.2 CDC-ACM Firmware Interface Functional Description                            1065
   29.3.3 USB-to-JTAG Interface: JTAG Command Processor                                1066
   29.3.4 USB-to-JTAG Interface: CMD_REP Usage Example                                 1067
   29.3.5 USB-to-JTAG Interface: Response Capture Unit                                 1068
   29.3.6 USB-to-JTAG Interface: Control Transfer Requests                            1068
29.4 Interrupts                                                                        1069
29.5 Programming Procedures                                                             1070
29.6 Register Summary                                                                  1072
29.7 Registers                                                                         1074

30 SDIO Slave Controller (SDIO)                                                       1100
30.1 Overview                                                                          1100
30.2 Features                                                                          1100
30.3 Architecture Overview                                                             1101
30.4 Standards Compliance                                                              1101
30.5 Functional Description                                                            1101
   30.5.1 Physical Bus                                                                 1101
   30.5.2 Supported Commands                                                           1102
   30.5.3 I/O Function 0 Address Space                                                  1102
   30.5.4 I/O Function 1/2 Address Space Map                                           1105
      30.5.4.1 Accessing SLC HOST Register Space                                      1105
      30.5.4.2 Transferring Incremental-Address Packets                               1106
      30.5.4.3 Transferring Fixed-Address Packets                                    1106
   30.5.5 DMA                                                                          1106
      30.5.5.1 Linked List                                                            1107
      30.5.5.2 Write-Back of Linked List                                              1109
      30.5.5.3 Data Padding and Discarding                                           1109
   30.5.6 SDIO Bus Timing                                                              1110
30.6 Interrupt                                                                         1111
   30.6.1 Host Interrupt                                                               1111
   30.6.2 Slave Interrupt                                                             1112
30.7 Packet Sending and Receiving Procedure                                          1112
```