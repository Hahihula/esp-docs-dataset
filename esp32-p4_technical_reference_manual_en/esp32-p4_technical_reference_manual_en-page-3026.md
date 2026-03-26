

```markdown
- receive the sampling enable signal from the timer.
- determine the conversion rules defined in the patterns for HP ADCx.
- drive the HP Readerx module to read conversion data.
- transfer conversion data to the filter.

• Filter: Filter0 and filter1, used for filtering conversion results in multi-channel sampling mode.
• Threshold Monitor: Threshold monitor 0 and threshold monitor 1 that trigger an interrupt when the filtered data is above a high threshold or below a low threshold.
• MODE_CNTL: Used for filtering the sampling signal triggered by the timer, supporting dual HP ADC sampling mode.
• HP Readerx: HP reader 1 and HP reader 2, driven by HP ADC FSMx to read data from HP ADCx.
• LP Readerx: LP reader 1 and LP reader 2, driven by LP ADCx Controller to read data from LP ADCx.
• LP ADCx Controller: LP ADC1 Controller and LP ADC2 Controller. The controllers provide sampling enable signal, drive the LP Readerx module to read the conversion results of LP ADCx, and store the conversion results.

## 62.5 Functional Description

### 62.5.1 SAR ADC Power Up

The SAR ADCs can be powered up by setting PMU_XPD_PERIF_I2C and PMU_PERIF_I2C_RST. The ADC sampling can be conducted immediately after power-up. Users need not be concerned about wait time, as it has been accounted for in the hardware design.

### 62.5.2 SAR ADC Channels

The SAR ADCs have 14 channels that are connected to 14 pins on the chip. To sample an analog signal, the SAR ADCs must first select the analog pin to measure via an internal multiplexer.

Table 62.5-1 shows the pins used as SAR ADC channels.

**Table 62.5-1. SAR ADC Channels and Chip Pins**

| Chip Pins | SAR ADC Channel | SAR ADC Selection |
|-----------|-----------------|-------------------|
| GPIO16    | 0               |                   |
| GPIO17    | 1               |                   |
| GPIO18    | 2               |                   |
| GPIO19    | 3               | SAR ADC1          |
| GPIO20    | 4               |                   |
| GPIO21    | 5               |                   |
| GPIO22    | 6               |                   |
| GPIO23    | 7               |                   |
| GPIO49    | 0               |                   |
| GPIO50    | 1               | SAR ADC2          |
```