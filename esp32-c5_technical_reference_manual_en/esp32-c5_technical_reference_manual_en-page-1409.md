

```markdown
Register 38.5. TWAIFD_BTR_REG (0x0024)

| 31 | 27 | 26 | 19 | 18 | 13 | 12 | 7 | 6 | 0 |
|-----:|:----|:----|:----|:----|:----|:----|:--|:--|:---|
|     | 0x2 | Oxa |    | 0x5 |    | 0x3 |   | 0x5 | Reset |

TWAIFD_PROP Configures the propagation segment for the nominal bit rate.
Measurement unit: Time quanta. (R/W)

TWAIFD_PH1 Configures the phase 1 segment for the nominal bit rate.
Measurement unit: Time quanta. (R/W)

TWAIFD_PH2 Configures the phase 2 segment for the nominal bit rate.
Measurement unit: Time quanta. (R/W)

TWAIFD_BRP Configures the baud-rate prescaler for the nominal bit rate.
Measurement unit: System clock period. (R/W)

TWAIFD_SJW Configures the synchronization jump width in the nominal bit time.
Measurement unit: Time quanta. (R/W)


Register 38.6. TWAIFD_BTR_FD_REG (0x0028)

| 31 | 27 | 26 | 19 | 18 | 17 | 13 | 12 | 11 | 7 | 6 | 5 | 0 |
|-----:|:----|:----|:----|:----|:-------|:----|:-------|:----|:--|:--|:--|:---|
|     | 0x2 | 0x4 |    | (reserved) | 0x3 |    | (reserved) | 0x3 | 0 |   | 0x3 | Reset |

TWAIFD_PROP_FD Configures the propagation segment for the data bit rate.
Measurement unit: Time quanta. (R/W)

TWAIFD_PH1_FD Configures the phase 1 segment for the data bit rate.
Measurement unit: Time quanta. (R/W)

TWAIFD_PH2_FD Configures the phase 2 segment for the data bit rate.
Measurement unit: Time quanta. (R/W)

TWAIFD_BRP_FD Configures the baud-rate prescaler for the data bit rate.
Measurement unit: Cycle of core clock. (R/W)

TWAIFD_SJW_FD Configures the synchronization jump width in data bit time.
Measurement unit: Time quanta. (R/W)
```