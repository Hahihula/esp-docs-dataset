

```markdown
42.4.11 Interrupts 2123
42.5 Programming Procedures 2124
42.5.1 Register Type 2124
42.5.2 Detailed Steps 2125
    42.5.2.1 Initializing UARTn 2125
    42.5.2.2 Configuring UARTn Communication 2125
    42.5.2.3 Enabling UARTn 2126
42.6 Register Summary 2127
    42.6.1 UART Register Summary 2127
    42.6.2 LP UART Register Summary 2128
    42.6.3 UHCI Register Summary 2129
42.7 Registers 2131
    42.7.1 UART Registers 2131
    42.7.2 LP UART Registers 2154
    42.7.3 UHCI Registers 2174

## 43 SPI Controller (SPI) 2196

43.1 Overview 2196
43.2 Glossary 2196
43.3 Features 2198
43.4 Architectural Overview 2200
43.5 Functional Description 2201
    43.5.1 Data Modes 2201
    43.5.2 Introduction to Bus Signals 2201
    43.5.3 Bit Read/Write Order Control 2204
    43.5.4 Unaligned Byte Transfer 2206
    43.5.5 Transfer Types 2206
    43.5.6 CPU-Controlled Data Transfer 2206
        43.5.6.1 CPU-Controlled Master Transfer 2207
        43.5.6.2 CPU-Controlled Slave Transfer 2209
    43.5.7 DMA-Controlled Data Transfer 2210
        43.5.7.1 DMA Configuration 2210
        43.5.7.2 DMA TX/RX Buffer Length Control 2211
    43.5.8 Data Flow Control (Take GP-SPI as an Example) 2212
        43.5.8.1 GP-SPI Functional Blocks 2212
        43.5.8.2 Data Flow Control as Master 2213
        43.5.8.3 Data Flow Control as Slave 2214
    43.5.9 GP-SPI as a Master 2215
        43.5.9.1 State Machine 2215
        43.5.9.2 Register Configuration for State and Bit Mode Control 2217
        43.5.9.3 Full-Duplex Communication (1-bit Mode Only) 2221
        43.5.9.4 Half-Duplex Communication (1/2/4/(8)-bit Mode) 2222
        43.5.9.5 DMA-Controlled Configurable Segmented Transfer 2224
    43.5.10 GP-SPI Works as a Slave 2228
        43.5.10.1 Configurable Communication Formats 2228
        43.5.10.2 CMD Values Supported in Half-Duplex Communication 2229
```