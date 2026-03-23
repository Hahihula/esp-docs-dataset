
```markdown
Register 15.9. RTC_WDT_SWD_WPROTECT_REG (0x0020)

RTC_WDT_SWD_WKEY    Configure this field to lock or unlock SWD’s configuration registers.
                    0x50D83AA1: unlock the SWD configuration register.
                    Others value: lock the SWD configuration register which can’t be modified by the software.
                    (R/W)


Register 15.10. RTC_WDT_INT_RAW_REG (0x0024)

RTC_WDT_SWD_INT_RAW    Represents the SWD whether or not generates timeout interrupt.
                       0: No
                       1: Yes
                       (R/WTC/SS)

RTC_WDT_INT_RAW        Represents the RWDT whether or not generates timeout interrupt.
                       0: No
                       1: Yes
                       (R/WTC/SS)
```