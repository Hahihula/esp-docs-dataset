**Title: Electrical Characteristics**

---

**Note:**  
The above ADC measurement range and accuracy are applicable to chips manufactured on and after the Date Code **342023** on shielding cases, or assembled on and after the D/C 1 and D/C 2 **2334** on bar-code labels. For chips manufactured or assembled earlier than these date codes, please ask our sales team to provide the actual range and accuracy according to batch.

For details of Date Code and D/C, please refer to [Espressif Chip Packaging Information](#).

---

### Section 5.5 Current Consumption

#### Subsection 5.5.1 RF Current Consumption in Active Mode

The current consumption measurements are taken with a **3.3 V** supply at **25 °C** of ambient temperature at the RF port. All transmitters' measurements are based on a **100% duty cycle**.

**Table 5-6: Bluetooth LE Current Consumption in Active Mode**

| Work Mode | Description                   | Peak (mA) |
|-----------|-------------------------------|-----------|
|           | TX                           |           |
| Active (RF working) | Bluetooth LE @ **20.0 dBm**   | **140**  |
|           |                               | **60**    |
|           |                               | **36**    |
|           |                               | **24**    |
| RX        | Bluetooth LE                 | **24**    |

---

#### Subsection 5.5.2 Current Consumption in Other Modes

The measurements below are applicable to ESP32-H2FH2S and ESP32-H2FH4S.

**Table 5-7: 802.15.4 Current Consumption in Active Mode**

| Work Mode | Description                   | Peak (mA) |
|-----------|-------------------------------|-----------|
|           | TX                           | **140**   |
| Active (RF working) | 802.15.4 @ **20.0 dBm**     | **60**    |
|           |                               | **36**    |
|           |                               | **24**    |
| RX        | 802.15.4 @ -**24.0 dBm**   | **24**    |
|           | 802.15.4                    | **25**    |

---

**Table 5-8: Current Consumption in Modem-sleep Mode**

| Work mode       | Frequency (MHz) | Description                   | Typ ¹ (mA) | Typ ¹ (mA) |
|-----------------|-----------------|-------------------------------|-----------|-----------|
|                 |                 | All Peripheral Clocks Disabled |           |           |
|                 | **96**          | CPU running                   | **10**    | **17**    |
|                 | **64**          | CPU in idle                    | **6**     | **13**    |
|                 |                |                               | **8**     | **13**    |
|                 |                |                               | **5**     | **10**    |

Modem-sleep²

---

Continued on next page.

Espressif Systems  
[Submit Documentation Feedback](#)

ESP32-H2 Series Datasheet v1.2