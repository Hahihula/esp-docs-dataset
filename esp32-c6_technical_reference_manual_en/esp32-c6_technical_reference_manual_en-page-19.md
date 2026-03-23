
```markdown
28.5.9.5 Configuration of Slave Segmented Transfer in Half-Duplex    852
28.5.9.6 Configuration of Slave Segmented Transfer in Full-Duplex    853


28.6 CS Setup Time and Hold Time Control                                 853

28.7 GP-SPI2 Clock Control                                              854
   28.7.1 Clock Phase and Polarity                                      855
   28.7.2 Clock Control as Master                                       857
   28.7.3 Clock Control as Slave                                        857

28.8 GP-SPI2 Timing Compensation                                        857

28.9 Interrupts                                                         859

28.10 Register Summary                                                   862

28.11 Registers                                                          863


29 I2C Controller (I2C)                                                 893

29.1 Overview                                                            893

29.2 Features                                                            893

29.3 I2C Architecture                                                     894

29.4 Functional Description                                              896
   29.4.1 Clock Configuration                                            896
   29.4.2 SCL and SDA Noise Filtering                                    897
   29.4.3 SCL Clock Stretching                                          897
   29.4.4 Generating SCL Pulses in Idle State                            897
   29.4.5 Synchronization                                                 898
   29.4.6 Open-Drain Output                                              899
   29.4.7 Timing Parameter Configuration                                 900
   29.4.8 Timeout Control                                                902
   29.4.9 Command Configuration                                         902
   29.4.10 TX/RX RAM Data Storage                                       903
   29.4.11 Data Conversion                                               904
   29.4.12 Addressing Mode                                               904
   29.4.13 R/W Bit Check in 10-bit Addressing Mode                       905
   29.4.14 To Start the I2C Controller                                   905

29.5 Functional differences between LP_I2C and I2C                      905

29.6 Programming Example                                                906
   29.6.1 I2Cmaster Writes to I2Cslave with a 7-bit Address in One Command Sequence    906
      29.6.1.1 Introduction                                             906
      29.6.1.2 Configuration Example                                    907
   29.6.2 I2Cmaster Writes to I2Cslave with a 10-bit Address in One Command Sequence    908
      29.6.2.1 Introduction                                             908
      29.6.2.2 Configuration Example                                    908
   29.6.3 I2Cmaster Writes to I2Cslave with Two 7-bit Addresses in One Command Sequence    909
      29.6.3.1 Introduction                                             910
      29.6.3.2 Configuration Example                                    910
   29.6.4 I2Cmaster Writes to I2Cslave with a 7-bit Address in Multiple Command Sequences    911
      29.6.4.1 Introduction                                             912
      29.6.4.2 Configuration Example                                    913
   29.6.5 I2Cmaster Reads I2Cslave with a 7-bit Address in One Command Sequence            914
```