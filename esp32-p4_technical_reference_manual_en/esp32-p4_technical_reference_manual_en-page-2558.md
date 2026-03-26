

```markdown
## 50.5.1 OTG Interface

The OTG_FS supports both the Session Request Protocol (SRP) and Host Negotiation Protocol (HNP) of the OTG Revision 1.3 specification. The OTG_FS controller core interfaces with the internal transceiver using the UTMI+ OTG interface. The UTMI+ OTG interface allows the controller core to manipulate the transceiver for OTG purposes, e.g., enabling/disabling pull-ups and pull-downs in HNP, and also allows the transceiver to indicate OTG related events. If an external transceiver is used instead, the UTMI+ OTG interface signals will be routed to the ESP32-P4's GPIOs instead through GPIO Matrix. Please refer to Chapter 9 GPIO Matrix and IO MUX. The UTMI+ OTG interface signals are described in Table 50.5-1.

Table 50.5-1. UTMI+ OTG Interface

| Signal Name             | I/O | Description                                                                                                                                                                                                 |
|-------------------------|-----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| usb_otg_iddig_in        | I   | Mini A/B Plug Indicator. Indicates whether the connected plug is mini-A or mini-B. Valid only when usb_otg_idpullup is sampled asserted.<br>0: Mini-A connected<br>1: Mini-B connected                                                                 |
| usb_otg_avalid_in       | I   | A-Peripheral Session Valid. Indicates if the voltage Vbus is at a valid level for an A-peripheral session. The comparator thresholds are:<br>0: Vbus < 0.8 V<br>1: Vbus = 0.2 V to 2.0 V                                                                 |
| usb_otg_bvalid_in       | I   | B-Peripheral Session Valid. Indicates if the voltage Vbus is at a valid level for a B-peripheral session. The comparator thresholds are:<br>0: Vbus < 0.8 V<br>1: Vbus = 0.8 V to 4 V                                                                 |
| usb_otg_vbusvalid_in    | I   | Vbus Valid. Indicates if the voltage Vbus is valid for A/B-device/peripheral operation. The comparator thresholds are:<br>0: Vbus < 4.4 V<br>1: Vbus > 4.75 V                                                                 |
| usb_srp_sessend_in      | I   | B-device Session End. Indicates if the voltage Vbus is below the B-device Session End threshold. The comparator thresholds are:<br>0: Vbus > 0.8 V<br>1: Vbus < 0.2 V                                                                 |
```