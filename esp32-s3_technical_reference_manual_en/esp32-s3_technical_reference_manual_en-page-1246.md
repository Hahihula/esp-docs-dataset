**Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Diagram Title and Description:**
Figure 33.3-1. USB Serial/JTAG and USB-OTG Internal/External PHY Routing Diagram

**Diagram Labels:**
- **USB OTG Logic**: 
  - `USB_OTG_Logic`
  - `usb otg internal PHY interface`

- **Internal PHY PAD (0)**:
  - `Internal PHY`
  - `PAD`

- **USB host directly connected to pads: D -> GPIO19, D+ -> GPIO20**

- **USB Device Logic**:
  - `USB_Device_Logic`
  - `usb otg external PHY interface`

- **GPIO Matrix PAD (1)**:
  - `GPIO Matrix`
  - `PAD`

- **External PHY connected to pads: VP -> MTMS, VM -> MTDI, OEN -> MDIO, VPO -> MTCK, VMO -> GPIO38**

**Diagram Control Registers and Signals:**
- `RTC_CNTL_SW_USB_PHY_SEL_REG` (0)
- `RTC_CNTL_SW_HW_USB_PHY_SEL_REG` —
- `efuse_usb_phy_sel` (0)

**Footer Information:**
Espressif Systems  
1246 ESP32-S3 TRM (Version 1.7)  

**Link Texts:**
- Submit Documentation Feedback

**Navigation Link:** 
GoBack