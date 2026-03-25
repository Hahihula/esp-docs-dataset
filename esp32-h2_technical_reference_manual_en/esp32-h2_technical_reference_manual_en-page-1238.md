

```markdown
Figure 40.5-2. DIG ADC FSM Block Diagram

Wherein:

*   Timer: a dedicated timer for the DIG ADC controller to generate `sample_start` signal.
*   pr: a pointer to the pattern table that defines the conversion rules for ADC. FSM sends out corresponding signals based on the conversion rules.

APB_SARADC_TIMER_EN can be set to enable the timer. The timeout event of this timer triggers a `sample_start` signal. This signal drives the FSM module to start sampling. When the FSM module receives the `sample_start` signal, it starts the following operations:

*   Powers up SAR ADC.
*   Determines the conversion rules (selected sample channels and attenuations) defined in the patterns that the current pr points to.
*   Outputs the en_pin and atten signals corresponding to the conversion rules to the analog side.
*   Initiates the sar_start signal and starts sampling.

When FSM receives the reader_done signal from Digital_reader, it starts the following operations:

*   Stops sampling.
*   Transfers the conversion result to the filter. Then the threshold monitor transfers the filtered result to memory via GDMA (see Figure 40.4-1).
*   Updates pr and waits for the next sampling. The pointer pr counts cyclically between 0 and APB_SARADC_SAR_PATT_LEN (table_length).
```