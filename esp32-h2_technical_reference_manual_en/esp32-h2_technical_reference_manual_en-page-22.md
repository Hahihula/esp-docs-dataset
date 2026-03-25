

```markdown
34.1 Features 986
34.2 Protocol Overview 987
34.2.1 TWAI Properties 987
34.2.2 TWAI Messages 988
    34.2.2.1 Data Frames and Remote Frames 988
    34.2.2.2 Error and Overload Frames 990
    34.2.2.3 Interframe Space 992
34.2.3 TWAI Errors 992
    34.2.3.1 Error Types 992
    34.2.3.2 Error States 993
    34.2.3.3 Error Counters 993
34.2.4 TWAI Bit Timing 994
    34.2.4.1 Nominal Bit 994
    34.2.4.2 Hard Synchronization and Resynchronization 995
34.3 Architectural Overview 996
34.3.1 Registers Block 997
34.3.2 Bit Stream Processor 998
34.3.3 Error Management Logic 998
34.3.4 Bit Timing Logic 998
34.3.5 Acceptance Filter 998
34.3.6 Receive FIFO 998
34.4 Functional Description 998
34.4.1 Modes 999
    34.4.1.1 Reset Mode 999
    34.4.1.2 Operation Mode 999
34.4.2 Bit Timing 999
34.4.3 Interrupt Management 1000
    34.4.3.1 Receive Interrupt (RXI) 1001
    34.4.3.2 Transmit Interrupt (TXI) 1001
    34.4.3.3 Error Warning Interrupt (EWI) 1001
    34.4.3.4 Data Overrun Interrupt (DOI) 1001
    34.4.3.5 Error Passive Interrupt (EPI) 1002
    34.4.3.6 Arbitration Lost Interrupt (ALI) 1002
    34.4.3.7 Bus Error Interrupt (BEI) 1002
    34.4.3.8 Bus Idle Status Interrupt (BISI) 1002
34.4.4 Transmit and Receive Buffers 1002
    34.4.4.1 Overview of Buffers 1002
    34.4.4.2 Frame Information 1003
    34.4.4.3 Frame Identifier 1004
    34.4.4.4 Frame Data 1005
34.4.5 Receive FIFO and Data Overruns 1005
34.4.6 Acceptance Filter 1006
    34.4.6.1 Single Filter Mode 1006
    34.4.6.2 Dual Filter Mode 1007
34.4.7 Error Management 1008
    34.4.7.1 Error Warning Limit 1009
```