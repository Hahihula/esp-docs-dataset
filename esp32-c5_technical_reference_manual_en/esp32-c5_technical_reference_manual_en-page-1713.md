

```markdown
Chapter 46 ADC Controller

The timer timeout will trigger DiG ADC FSM to start sampling according to the pattern table. The conversion result will be automatically stored in memory. When the sampling reaches the number of limit set in APB_SARADC_APB_ADC_EOF_NUM, it will terminate.

Once sampling is complete, an APB_SARADC_ADC_DONE_INT_RAW interrupt will be generated.
```