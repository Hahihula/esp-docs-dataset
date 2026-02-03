**Title: Chapter 32 USB On-The-Go (USB)**

---

### Figure Caption:
Figure 32.4-1. A-Device SRP  
is set in Global Interrupt Status register.

6. The application must service the Session Request Detected interrupt and turn on the Port Power bit by writing the Port Power bit in the Host Port Control and Status register. The PHY indicates port power-on by asserting `usb_otg_vbusvalid_in` signal.
7. When the USB is powered, the B-device connects, completing the SRP process.

---

### Subtitle: 32.4.3.2 B-Device SRP

**Body Text:**  
Figure 32.4-2 illustrates the flow of SRP when the OTG_FS is acting as a B-device (i.e., does not power Vbus).

1. To save power, the host (A-device) suspends and turns off port power when the bus is idle. PHY indicates port power off by deasserting the `usb_otg_vbusvalid_in` signal. The OTG_FS core sets the Early Suspend bit in the Core Interrupt register (`USB_ERLYSUSP interrupt`) after detecting 3 ms of bus idleness.

---

### Diagrams:
- **Figure 32.4-1: A-Device SRP**
  - `usb_otg_drvbus`
    - suspend
      - 1 (D+)
      - 6 (Vbus pulsing)

  - `usb_otg_vbusvalid_in` 
    - 2

  - `usb_otg_availd_in`
    - 5 Vbus pulsing

  - D- line with Data line pulsing
    - 3, 4
  
  - Connect (7)
  
- **Figure 32.4-2: B-Device SRP**
  - `usb_otg_vbusvalid_in` 
    - suspend
      - 1 (D+)

  - `usb_otg_bvalid_in`
    - 2

  - `usb_srp_dischrgvbus`
    - 3
  
  - `usb_srp_sessend_in`
    - 4
  
  - D- line with Data line pulsing
    - 5
  
  - Connect (7)
  
  - VBUS pulsing for `usb_otg_chrgvbus`