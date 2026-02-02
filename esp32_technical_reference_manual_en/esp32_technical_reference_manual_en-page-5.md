**Contents**

### I Microprocessor and Master

1 **ULP Coprocessor (ULP)**
   - [1.1 Introduction](#ulpcoprocessor-ulp-introduction)
     - 29
   - [1.2 Features](#ulpcoprocessor-ulp-features)
     - 29
   - [1.3 Functional Description](#ulpcoprocessor-ulp-functional-description)
     - 30
   - [1.4 Instruction Set](#ulpcoprocessor-ulp-instruction-set)
     - 30

     - **1.4.1 ALU - Perform Arithmetic/Logic Operations**
       - 1.4.1.1 Operations Among Registers (page: 31)
       - 1.4.1.2 Operations with Immediate Value (page: 31)
       - 1.4.1.3 Operations with Stage Count Register (page: 32)
     - **1.4.2 ST – Store Data in Memory** (page: 33)
     - **1.4.3 LD – Load Data from Memory** (page: 34)
     - **1.4.4 JUMP – Jump to an Absolute Address** (page: 35)
     - **1.4.5 JUMPR – Jump to a Relative Offset (Conditional upon RO)** (page: 35)
     - **1.4.6 JUMPS – Jump to a Relative Address (Conditional upon Stage Count Register)** (page: 36)
     - **1.4.7 HALT – End the Program** (page: 36)
     - **1.4.8 WAKE – Wake up the Chip** (page: 36)
     - **1.4.9 Sleep – Set the ULP Timer’s Wake-up Period** (page: 37)
     - **1.4.10 WAIT – Wait for a Number of Cycles** (page: 37)
     - **1.4.11 ADC – Take Measurement with ADC** (page: 37)
     - **1.4.12 I2C_RD/I2C_WR – Read/Write I2C** (page: 38)
     - **1.4.13 REG_RD – Read from Peripheral Register** (page: 39)
     - **1.4.14 REG_WR – Write to Peripheral Register** (page: 39)

   - [1.5 ULP Program Execution](#ulpcoprocessor-ulp-program-execution) (page: 40)
   
   - [1.6 RTC_I2C Controller]
     - **1.6.1 Configuring RTC-I2C** (page: 41)
     - **1.6.2 Using RTC_I2C**
       - 1.6.2.1 I2C RD – Read a Single Byte
       - 1.6.2.2 I2C_WR – Write a Single Byte
       - 1.6.2.3 Detecting Error Conditions (page: 43)
     - **1.6.4 Connecting I2C Signals** (page: 44)

   - [1.7 Register Summary]
     - **1.7.1 SENS_ULP Address Space**
       - 1.7.2 RTC_I2C Address Space
     - **1.8 Registers**
       - **1.8.1 SENS_ULP Address Space** (page: 47)
       - **1.8.2 RTC_I2C Address Space**

### II DMA Controller (DMA)

- [2.1 Overview](#dmacontroller-dma-overview) 
- [2.2 Features] 

---

Espressif Systems  
ESP32 TRM (Version 5.6)  

[Submit Documentation Feedback](#)