

```markdown
Chapter 62 ADC Controller (ADC)  
GoBack

3. Configure `LPADC_SARx_WAKEUP_TH_HIGH` and `LPADC_SARx_WAKEUP_TH_LOW` to set the high and low thresholds.
4. Set `LPADC_SARx_WAKEUP_EN` to enable automatic monitoring.
5. Set `LPADC_ADCx_HW_READ_EN_I` to enable periodic monitoring.

During the automatic monitoring process, the conversion data will not be stored, but software can always read the last conversion data from `LPADC_SAR_MEASn_DATA_SAR`.

Espressif Systems    3035    Submit Documentation Feedback    ESP32-P4 TRM PRELIMINARY
```