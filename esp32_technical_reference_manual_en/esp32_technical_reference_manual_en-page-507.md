**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.19. EMACFC_REG (0x1018)

**Navigation Link:**
GoBack

**Continuation Notice:**
Continued from the previous page...

**Subsection Title and Description:**
FCBBA
This bit initiates a Pause frame in the full-duplex mode and activates the backpressure function in the half-duplex mode if the TFCE bit is set. In the full-duplex mode, this bit should be read as 1'b0 before writing to the Flow Control register.

**Body Text:**
To initiate a Pause frame, the Application must set this bit to 1'b1. During a transfer of the Control Frame, this bit continues to be set to signify that a frame transmission is in progress. After the completion of Pause frame transmission, the MAC resets this bit to 1'b0.

The Flow Control register should not be written until after all bits are cleared.
In half-duplex mode, when this bit (and TFCE) is set), then backpressure is asserted by the MAC during backpressure; When the MAC receives a new frame,
the transmitter starts sending JAM pattern resulting in collision. The R/W/SC(FCB)/(R/W)(BPA(backpressure activate)).

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32 TRM (Version 5.6)