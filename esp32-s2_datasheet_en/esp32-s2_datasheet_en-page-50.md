**Title: Electrical Characteristics**

---

### Table 5-5. ADC Characteristics

| Symbol | Parameter | Min | Max | Unit |
|--------|-----------|-----|-----|------|
| DNL (Differential nonlinearity)¹ | ADC connected to an external 100 nF capacitor; DC signal input: Ambient temperature at 25 °C; Wi-Fi off | –7 | 7 | LSB |
| INL (Integral Nonlinearity) | — | –12 | 12 | LSB |
| Sampling rate | To get better DNL results, you can sample multiple times and apply a filter, or calculate the average value. kSPS means kilo samples-per-second. | — | 100 | kSPS² |

**Note:**
When reading voltages greater than 2450 mV, ADC accuracy will be worse than that in the table above.

The calibrated ADC results after hardware calibration and software calibration are shown in Table 5-6. For higher accuracy, you may implement your own calibration methods.

---

### Table 5-6. ADC Calibration Results

| Parameter | Description | Min | Max | Unit |
|-----------|-------------|-----|-----|------|
| ATTN0, effective measurement range of 0 ~ 700 | — | –10 | 10 | mV |
| ATTN1, effective measurement range of 0 ~ 950 | — | –11 | 11 | mV |
| Total error | — | — | — | — |
| ATTN2, effective measurement range of 0 ~ 1200 | — | –13 | 13 | mV |
| ATTN3, effective measurement range of 0 ~ 2300 | — | –17 | 17 | mV |

**Note:**
The above ADC measurement range and accuracy are applicable to chips manufactured on and after the Date Code (see bar-code labels). For chips with shielding cases or assembled before these date codes, please ask our sales team for actual range according to batch.

For details of Date Code D/C 1203/2479568, refer to [Espressif Chip Packaging Information](#).

---

**Section: Current Consumption**

### Subsection: RF Current Consumption in Active Mode

The current consumption measurements are taken with a 3.3 V supply at 25 °C of ambient temperature at the RF port. All transmitters' measurements are based on a 100% duty cycle.

---

*Espressif Systems*
*ESP32-S2 Series Datasheet v1.8*

[Submit Documentation Feedback](#)