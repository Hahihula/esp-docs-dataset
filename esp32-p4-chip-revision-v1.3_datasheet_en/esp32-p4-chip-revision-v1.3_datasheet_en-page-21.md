**Title: Table 2-3 – cont’d from previous page**

**Table Headers:**  
Pin No., IO MUX / GPIO Name, FO Type F1, Type F2, Type F3, Type

| Pin No. | IO MUX / GPIO Name | FO Type   | I/O/T | I/O/T | GMAC_PHY_TXEN_PAD  | O |
|---------|--------------------|----------|------|------|---------------------|---|
| 92      | GPIO49             | GPIO49   | I/O/T | I/O/T | GMAc_PHY_TXEN_PAD   | - |
| 93      | GPIO50             | GPIO50   | I/O/T | I/O/T | GMAC_RMII_CLK_PAD   | IO |
| 94      | GPIO51             | GPIO51   | I/O/T | I/O/T | GMAc_PHY_RXDV_PAD   | - |
| 95      | GPIO52             | GPIO52   | I/O/T | I/O/T | GMAC_PHY_RXDO_PAD   | IO |
| 97      | GPIO53             | GPIO53   | I/O/T | I/O/T | GMAc_PHY_RXD1_PAD   | - |
| 98      | GPIO54             | GPIO54   | I/O/T | I/O/T | GMAC_PHT_RXER_PAD   | IO |
| 104     | GPIO00             | GPIO00   | I/O/T | I/O/T |                    | - |

**Footnotes:**
1. Bold marks the default pin function in the default boot mode. See Section **3.1 Chip Boot Mode Control**.
2. Regarding highlighted cells, see Section 2.8.4 Restrictions for GPIOs and LP GPIOs.

**Additional Information:**  
Each IO MUX function (Fn, n = 0-3) is associated with a type. The description of type as follows:
- I – input; O – output; T – high impedance.
- l1 – input; if the pin is assigned a function other than Fn, the input signal of Fn is always 1.
- IO – input; if the pin is assigned a function other than Fn, the input signal of Fn is always θ.

**Document Footer:**  
ESP32-P4 Series Datasheet v0.6

**Watermark Text:**
PRIVATARY