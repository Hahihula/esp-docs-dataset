**Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Diagram Title and Description:**
Figure 33.2-2. USB Serial/JTAG Block Diagram

**Diagram Content:**
- **Host**: 
  - Connected to EP_0, Control logic, Descriptor ROM
  - Connected to USB PHY (internal/external)
    - Further connected to USB protocol engine
  
- **EP OUT_1**, **EPIN_1**, **EPIN_2**, and **EPIN_3**:
  - EP OUT_1 is also linked with CDC_ACM ep, which connects To CPU: Registers Interrupts
  - JTAG out from EP OUT_2 connected to CPU/JTAG interface
  
- Text below diagram explains routing options for internal PHY usage via GPIO matrix or adding an external USB PHY.

**Text Below Diagram Explanation:**
Either one of these can use the internal PHY. Optionally, the signals from the unit not using the internal PHY can be routed out via the GPIO matrix to IO pads. Adding an external USB PHY to these pads results in a second usable USB port.
The actual routing from USB Serial/JTAG Controller and USB-OTG to internal and external PHYs initially is decided using eFuses as described in Table 33.4-1. This configuration can later be modified using register writes.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**GoBack Link:** 
GoBack