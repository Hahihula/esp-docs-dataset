**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**GoBack Link:** [GoBack](#)

**List of Components and Features in the Chapter:**
- SDA data controller (SCL_MAIN_FSM)
- serial/parallel data converter (DATA_Shifter)
- filter for SCL (SCL_Filter)
- filter for SDA (SDA_Filter)

**Body Text Explanation:**
Besides, the I2C controller also has a clock module which generates I2C clocks, and a synchronization module which synchronizes the APB bus and the I2C controller.

The clock module is used to select clock sources, turn on and off clocks, and divide clocks. SCL_Filter and SDA_Filter remove noises on SCL input signals and SDA input signals respectively. The synchronization module synchronizes signal transfer between different clock domains.

**Figure References:**
- Figure 27.3-3
- Figure 27.3-4

These figures show the timing diagram and corresponding parameters of the I2C protocol, with SCL_FSM generating a sequence conforming to the I2C protocol.
- **SCL_MAIN_FSM** controls the execution of I2C commands and sequences on the SDA line: CMD_Controller is used for an I2C master to generate (R)START, STOP, WRITE, READ, and END commands. TX RAM and RX RAM store data to be transmitted; data received respectively.
- **DATA_Shifter** shifts data between serial and parallel form.

**Figure Caption with Diagram Description:** 
"Figure 27.3-3: I2C Protocol Timing (Cited from Fig.31 in The I2C-bus Specification Version 2.1)"

**Diagram Details for Figure Reference:**
The diagram shows the definition of timing for F/S-mode devices on the I²C-bus, with various signals labeled such as SDA, SCL, and different states like HD/STA.

**Footer Information:** 
- Page Number: 987
- Company Name: Espressif Systems
- Document Title: ESP32-S3 TRM (Version 1.7)
- Link for Submitting Documentation Feedback