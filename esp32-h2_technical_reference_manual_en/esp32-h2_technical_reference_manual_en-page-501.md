

```markdown
Register 14.9. RTC_WDT_SWDPWPROTECT_REG (0x0024)

RTC_WDT_SWDPWKEY Configure this field to lock or unlock SWD's configuration registers.
0x50D83AA1: unlock the SWD configuration register.
Other values: lock the SWD configuration register which can't be modified by the software.
(R/W)
```

```markdown
Register 14.10. RTC_WDT_INT_RAW_REG (0x0028)

RTC_WDT_SWDPWINT_RAW Represents the SWD whether or not generates timeout interrupt.
0: No
1: Yes
(R/W/TC/SS)

RTC_WDT_INT_RAW Represents the RWDT whether or not generates timeout interrupt.
0: No
1: Yes
(R/W/TC/SS)
```