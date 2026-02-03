**Chapter Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Tables and Their Descriptions:**

1. **Table 33.4-3. Reset SoC into Download Mode**
   - Columns:
     - Action
     - Internal state
     - Note
   - Rows:
     | Action                | Internal state       | Note                                    |
     |-----------------------|----------------------|----------------------------------------|
     | Clear DTR             | RTS=?, DTR=0        | Initialize to known values              |
     | Clear RTS             | RTS=0, DTR=0        | -                                      |
     | Set DTR               | RTS=0, DTR=1        | Set download mode flag                  |
     | Clear RTS             | RTS=0, DTR=1        | Propagate DTR                           |
     | Set RTS               | RTS=1, DTR=0        | -                                      |
     | Clear RTS             | RTS=1, DTR=0        | Reset SoC                              |
     | Set RTS               | RTS=1, DTR=1        | Propagate DTR                           |
     | Clear RTS             | RTS=0, DTR=0        | Clear download flag                     |

2. **Table 33.4-4. Reset SoC into Booting**
   - Columns:
     - Action
     - Internal state       | Note                                    |
   - Rows:
     | Action                | Internal state       | Note                                    |
     |-----------------------|----------------------|----------------------------------------|
     | Clear DTR             | RTS=?, DTR=0        | -                                      |
     | Clear RTS             | RTS=0, DTR=0        | Clear download flag                     |
     | Set RTS               | RTS=1, DTR=0        | Reset SoC                              |
     | Clear RTS             | RTS=0, DTR=0        | Exit reset                              |

**Additional Text:**
"To reset the SoC into booting from flash:"

**Footer Information:**
- Page number and document version:
  - "1254 ESP32-S3 TRM (Version 1.7)"
  
**Company Name:**
- Espressif Systems

**Link for Feedback Submission:**
- Submit Documentation Feedback