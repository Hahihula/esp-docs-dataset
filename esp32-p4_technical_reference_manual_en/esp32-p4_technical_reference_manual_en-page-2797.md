

```markdown
Register 55.14. LEDC_TIMERx_CNT_CAP_REG (x: 0-3) (0x0150+0x4*x)

LEDC_TIMERx_CNT_CAP Represents the captured LEDC timer x count value. (RO)


Register 55.15. LEDC_INT_RAW_REG (0x00CO)
```

```markdown
LEDC_TIMERx_OVF_INT_RAW (x: 0-3) Raw status bit: The raw interrupt status of LEDC_TIMERx_OVF_INT. Triggered when the timer x has reached its maximum counter value. (R/WTC/SS)

LEDC_DUTY_CHNG_END_Ch_n_INT_RAW (n: 0-7) Raw status bit: The raw interrupt status of LEDC_DUTY_CHNG_END_Ch_n_INT. Triggered when the fading of duty has finished. (R/WTC/SS)

LEDC_OVF_CNT_Ch_n_INT_RAW (n: 0-7) Raw status bit: The raw interrupt status of LEDC_OVF_CNT_Ch_n_INT. Triggered when the ovf_cnt has reached the value specified by LEDC_OVF_NUM_Ch_n. (R/WTC/SS)
```