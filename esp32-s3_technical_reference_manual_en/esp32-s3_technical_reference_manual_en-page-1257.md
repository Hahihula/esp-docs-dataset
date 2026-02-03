**Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Back Link:**
GoBack

**Subheading and Register Information:**
Register 33.3. USB_SERIAL_JTAG_CONFO_REG (0x0018)

**Binary Representation Table with Labels for Each Bit:**
- Bits are labeled from right to left as follows:
  - USB_SERIAL_JTAG_USB_PAD_ENABLE
  - USB_SERIAL_JTAG_USB_PULLDOWN
  - USB_SERIAL_JTAG_USB_PULLUP
  - USB_SERIAL_JTAG_USB_EDGE_SEL
  - (reserved)
  - USB_SERIAL_JTAG_USB_BRIDGE_EN

**Description of Register:**
USB_SERIAL_JTAG_PHY_SSEL Select internal/external PHY. '1'b0: internal PHY, '1'b1: external PHY.
(R/W)

**Other Registers and Their Functions with Access Type Indication in Parentheses (R/W):**

- USB_SERIAL_JTAG_EXCHG_PINS_OVERRIDE Enable software control USB D+ D- exchange. (R/W)
- USB_SERIAL_JTAG_EXCHG_pins USB D+ D- exchange. (R/W)
- USB_SERIAL_JTAG_VREFH Control single-end input high threshold, 1.76 V to 2 V, step 80 mV.
(R/W)

- USB_SERIAL_JTAG_VREFL Control single-end input low threshold, 0.8 V to 1.04 V, step 80 mV.

**Additional Registers:**

- USB_SERIAL_JTAG_VREF OVERRIDE Enable software control input threshold (R/W)
- USB_SERIAL_JTAG_PAD_PULLUP OVERRIDE Enable software control USB D+ pullup.
(R/W)

- USB_SERIAL_JTAG_DP_PULLUP Control USB D+ pull up. (R/W)
- USB_SERIAL_JTAG_DP_PULLDOWN Control USB D+ pull down.

- USB_SERIAL_JTAG_DM_PULLUP Control USB D- pull up. (R/W)
- USB_SERIAL_JTAG_DM_PULLDOWN Control USB D- pull down.
(R/W)

- USB_SERIAL_JTAG_PULLUP_VALUE Control pull up value: 0: 2.2 K; 1: 1.1 K.

- USB_SERIAL_JTAG_USB_PAD_ENABLE Enable USB pad function (R/W)
- USB_SERIAL_JTAG_PHY_TX_EDGE_SEL Tx output at clock negedge.
(R/W)

**Bit Description for USB_SERIAL_JTAG_USB_BRIDGE_EN Bit:**
Set this bit usb_jtag, the connection between usb_jtag and internal JTAG is disconnected, and MTMS, MTDI, MTCOK are output through GPIO Matrix. MTDO is input through GPIO Matrix.

**Footer Information:**
Espressif Systems
1257 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback