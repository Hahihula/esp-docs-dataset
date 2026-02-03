**Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Subtitle:**
Register 33.6. USB_SERIAL_JTAG_INT_RAW_REG (0x008)

**Body Text with Descriptions of Interrupts and Their Conditions in Register:**

- **USB_SERIAL_JTAG_IN_FLUSH_INT_RAW**: The raw interrupt bit turns to high level when flush cmd is received for IN endpoint 2 of JTAG.
- **USB_SERIAL_JTAG_SOF_IN_RAW**: The raw interrupt bit turns to high level when SOF frame is received. (R/WTC/SS)
- **USB_SERIAL_JTAG_SERIAL_OUT RECEV_PKT_INT_RAW**: The raw interrupt bit turns to high level when Serial Port OUT Endpoint received one packet.
  - Condition: When Serial Port OUT Endpoint receives a single data packet, the corresponding interrupt will be triggered and set its status flag. (R/WTC/SS)
- **USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT_RAW**: The raw interrupt bit turns to high level when Serial Port IN Endpoint is empty.
  - Condition: If there are no incoming packets on the serial port's input endpoint, this interrupt will be triggered and set its status flag. (R/WTC/SS)
- **USB_SERIAL_JTAG_PID_ERR_INT_RAW**: The raw interrupt bit turns to high level when PID error is detected.
  - Condition: When a parity check fails or there are other issues with the packet integrity on the serial port, this interrupt will be triggered and set its status flag. (R/WTC/SS)
- **USB_SERIAL_JTAG_CRC5_ERR_INT_RAW**: The raw interrupt bit turns to high level when CRC5 error is detected.
  - Condition: When a CRC5 check fails or there are other issues with the packet integrity on the serial port, this interrupt will be triggered and set its status flag. (R/WTC/SS)
- **USB_SERIAL_JTAG_CRC16_ERR_INT_RAW**: The raw interrupt bit turns to high level when CRC16 error is detected.
  - Condition: When a CRC16 check fails or there are other issues with the packet integrity on the serial port, this interrupt will be triggered and set its status flag. (R/WTC/SS)
- **USB_SERIAL_JTAG_STUFF_ERR_INT_RAW**: The raw interrupt bit turns to high level when stuff error is detected.
  - Condition: When a stuffing or unstuffing issue occurs during data transmission on the serial port, this interrupt will be triggered and set its status flag. (R/WTC/SS)
- **USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT_RAW**: The raw interrupt bit turns to high level when IN token for IN endpoint 1 is received.
  - Condition: When an IN token signal occurs on the input side of Endpoint 1, this interrupt will be triggered and set its status flag. (R/WTC/SS)
- **USB_SERIAL_JTAG_USB BUS_RESET_INT_RAW**: The raw interrupt bit turns to high level when USB bus reset is detected.
  - Condition: If a hardware or software-induced USB bus reset occurs on the system connected via JTAG, this interrupt will be triggered and set its status flag. (R/WTC/SS)
- **USB_SERIAL_JTAG_OUT EP1 ZERO_PAYLOAD_INT_RAW**: The raw interrupt bit turns to high level when OUT endpoint 1 received packet with zero payload.
  - Condition: When an OUT packet on Endpoint 1 is sent without any data, this interrupt will be triggered and set its status flag. (R/WTC/SS)
- **USB_SERIAL_JTAG_OUT EP2 ZERO_PAYLOAD_INT_RAW**: The raw interrupt bit turns to high level when OUT endpoint 2 received packet with zero payload.
  - Condition: When an OUT packet on Endpoint 2 is sent without any data, this interrupt will be triggered and set its status flag. (R/WTC/SS)

**Footer Information:**
Espressif Systems
1259 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback