
```markdown
27.71    Clock Phase and Polarity                                 640
27.7.2   Clock Control in Master Mode                             642
27.7.3   Clock Control in Slave Mode                              642
27.8     GP-SPI2 Timing Compensation                               642
27.9     Interrupts                                               644
27.10    Register Summary                                         647
27.11    Registers                                                648

28 I2C Controller (I2C)                                          676
28.1     Overview                                                 676
28.2     Features                                                 676
28.3     I2C Architecture                                         677
28.4     Functional Description                                    679
         28.4.1   Clock Configuration                              679
         28.4.2   SCL and SDA Noise Filtering                      679
         28.4.3   SCL Clock Stretching                             680
         28.4.4   Generating SCL Pulses in Idle State               680
         28.4.5   Synchronization                                   680
         28.4.6   Open-Drain Output                                 681
         28.4.7   Timing Parameter Configuration                   682
         28.4.8   Timeout Control                                   683
         28.4.9   Command Configuration                            684
         28.4.10  TX/RX RAM Data Storage                           685
         28.4.11  Data Conversion                                  686
         28.4.12  Addressing Mode                                   686
         28.4.13  R/W Bit Check in 10-bit Addressing Mode           687
         28.4.14  To Start the I2C Controller                       687
28.5     Programming Example                                      687
         28.5.1   I2Cmaster Writes to I2Cslave with a 7-bit Address in One Command Sequence
                   28.5.1.1 Introduction                           688
                   28.5.1.2 Configuration Example                 688
         28.5.2   I2Cmaster Writes to I2Cslave with a 10-bit Address in One Command Sequence
                   28.5.2.1 Introduction                           690
                   28.5.2.2 Configuration Example                 690
         28.5.3   I2Cmaster Writes to I2Cslave with Two 7-bit Addresses in One Command Sequence
                   28.5.3.1 Introduction                           692
                   28.5.3.2 Configuration Example                 692
         28.5.4   I2Cmaster Writes to I2Cslave with a 7-bit Address in Multiple Command Sequences
                   28.5.4.1 Introduction                           694
                   28.5.4.2 Configuration Example                 695
         28.5.5   I2Cmaster Reads I2Cslave with a 7-bit Address in One Command Sequence
                   28.5.5.1 Introduction                           696
                   28.5.5.2 Configuration Example                 697
         28.5.6   I2Cmaster Reads I2Cslave with a 10-bit Address in One Command Sequence
                   28.5.6.1 Introduction                           698
                   28.5.6.2 Configuration Example                 699
```