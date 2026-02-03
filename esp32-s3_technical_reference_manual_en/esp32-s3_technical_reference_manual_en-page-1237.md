Title: Chapter 32 USB On-The-Go (USB)

Subtitle: GoBack

Section Title: 32.4 OTG

Body Text:
USB OTG allows OTG devices to act in the USB Host role or the USB Device role. Thus, OTG devices will typically have a Mini-AB or Micro-AB receptacle so that it can receive an A-plug or B-plug. OTG devices will become either an A-device or a B-device depending on whether an A-plug or a B-plug is connected.

- A-device defaults to the Host role (A-Host) whilst B-device defaults to the Device role (B-Peripheral).
- A-device and B-device may exchange roles by using the Host Negotiation Protocol (HNP), thus becoming A-peripheral and B-Host.
- A-device can turn off Vbus to save power. B-device can then wake up the A-device by requesting it to turn on Vbus and start a new session. This mechanism is called session request protocol (SRP).
- A-device always powers Vbus even if it is an A-peripheral.

OTG devices are able to determine whether they are connected to an A plug or B plug using the ID pin of the plugs. The ID pin in A-plugs are pulled to ground whilst B-plugs have the ID pin left floating.

Section Title: 32.4.1 OTG Interface

Body Text:
The OTG_FS supports both the Session Request Protocol (SRP) and Host Negotiation Protocol (HNP) of the OTG Revision 1.3 specification. The OTG_FS controller core interfaces with the transceiver (internal or external) using the UTM+ OTG interface. The UTM+ OTG interface allows the controller core to manipulate the transceiver for OTG purposes (e.g., enabling/disabling pull-ups and pull-downs in HNP), and also allows the transceiver to indicate OTG related events. If an external transceiver is used instead, the UTM+ OTG interface signals will be routed to the ESP32-S3's GPIOs instead through GPIO Matrix, please refer to Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX). The UTM+ OTG interface signals are described in Table 32.4-1.

Table Title: Table 32.4-1. UMTI OTG Interface

Table:
| Signal Name | I/O | Description |
|-------------|-----|-------------|
| usb_otg_iddig_in | - | Mini A/B Plug Indicator. Indicates whether the connected plug is mini-A or mini-B. Valid only when usb_otg_idpullup is sampled asserted. |
| usb_otg_availd_in | 1'0: Mini-A connected | |
| usb_otg_bvalid_in | B-Peripheral Session Valid. Indicates if the voltage Vbus is at a valid level for a B-peripheral session. The comparator thresholds are: 1'b0: Vbus <0.8 V, 1'b1: Vbus = 0.2 V to 2.0 V |
| usb_otg_vvalid_in | - | Vbus Valid. Indicates if the voltage Vbus is valid for A/B-device/peripheral operation. The comparator thresholds are: 1'b0: Vbus <4.4 V, 1'b1: Vbus >4.75 V |

Footer:
Espressif Systems
Page Number: 1237
Document Title: ESP32-S3 TRM (Version 1.7)
Feedback Link Text: Submit Documentation Feedback