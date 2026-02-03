**Chapter Title:**
Chapter 32 USB On-The-Go (USB)

**Section Heading and Subsection with Content:**

#### Section:
32.4.4 B-Device HNP

##### Figure Caption for Flowchart in the Text:

Figure **32.4-4**: illustrates the flow of HNP when the OTG_FS is acting as an A-device.

##### Diagram Description (Flowchart):
The diagram shows a sequence with labels indicating different states and actions:
- Device
  - Suspend -> D+
    - Steps: 1, 2, 3, 4, 5, 6, 7, Traffic
    - Actions include "Connect" at step 8.
- Host

##### Figure Caption for Diagram in the Text:

Figure **32.4-4**: B-Device HNP

##### Detailed Description of Steps:
1. The A-device sends the SetFeature b_hnp_enable descriptor to enable HNP support. The OTG_FS core’s ACK response indicates that it supports HNP. The application must set the Device HNP Enable bit (USB_DEVHNPEN) in the OTG Control and Status register to indicate HNP support. The application sets the HNP Request bit (USB_DEVHNPEN) in the OTG Control and Status register to indicate to the OTG_FS core that it should initiate a Host Negotiation Process.

**Additional Information:**
- GoBack
- Submit Documentation Feedback

**Footer Text:** 
Espressif Systems  
1241  
ESP32-S3 TRM (Version 1.7)